# Automation-Mikrotik-
Automation aimed at managing networks on Mikrotik Routerboard
in MikroTik Scripting Language!!!

#Verifica e avisa via log quando a MikroTik estiver com uso maior que 80%:
:local cpuUsage [/system resource get cpu-load]

:if ($cpuUsage < 80) do={
    :log warning ("Alerta: Uso de CPU acima de 80%! Uso atual: " . $cpuUsage . "%")
}
