# flujo-de-datos
export default function DashboardPage() {
  return (
    <main className="min-h-screen bg-slate-50 p-6">
      <div className="mx-auto max-w-7xl space-y-6">
        <header className="flex items-center justify-between rounded-2xl bg-white p-4 shadow-sm border border-slate-200">
          <div>
            <h1 className="text-2xl font-bold text-slate-800">Dashboard Ejecutivo</h1>
            <p className="text-sm text-slate-500">Datos extraídos del Excel</p>
          </div>

          <div className="flex gap-3">
            <button className="rounded-lg border border-slate-200 px-4 py-2 text-sm">Últimos 30 días</button>
            <button className="rounded-lg bg-blue-600 px-4 py-2 text-sm text-white">Exportar CSV</button>
          </div>
        </header>

        <section className="grid gap-4 md:grid-cols-4">
          <StatCard title="Ventas totales" value="$245,800" change="+12.4%" />
          <StatCard title="Margen" value="28.6%" change="+2.1%" />
          <StatCard title="Pedidos" value="1,248" change="+8.7%" />
          <StatCard title="Conversión" value="6.4%" change="+1.3%" />
        </section>

        <section className="grid gap-6 lg:grid-cols-3">
          <div className="lg:col-span-2 rounded-2xl bg-white p-4 shadow-sm border border-slate-200">
            <h2 className="mb-4 text-lg font-semibold">Ventas por mes</h2>
            {/* RevenueChart */}
          </div>
          <div className="rounded-2xl bg-white p-4 shadow-sm border border-slate-200">
            <h2 className="mb-4 text-lg font-semibold">Canales</h2>
            {/* ChannelChart */}
          </div>
        </section>

        <section className="rounded-2xl bg-white p-4 shadow-sm border border-slate-200">
          <h2 className="mb-4 text-lg font-semibold">Detalle de ventas</h2>
          {/* SalesTable */}
        </section>
      </div>
    </main>
  );
}
