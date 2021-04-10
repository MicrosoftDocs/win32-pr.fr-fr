---
title: Fonctions de l’interface de protocole de routage
description: Implémentez les fonctions suivantes pour une DLL de protocole de routage
ms.assetid: fd780458-ef23-4ef2-8fe8-29b32100917f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b696d516cf0fc0b13d66fdc53b384a28fac8696a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941322"
---
# <a name="routing-protocol-interface-functions"></a>Fonctions de l’interface de protocole de routage

Implémentez les fonctions suivantes pour une DLL de protocole de routage :

[**AddInterface**](/windows/desktop/api/Routprot/nc-routprot-padd_interface)

[**ConnectClient**](/windows/desktop/api/Routprot/nc-routprot-pconnect_client)

[**DeleteInterface**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface)

[**DisconnectClient**](/windows/desktop/api/Routprot/nc-routprot-pdisconnect_client)

[**DoUpdateRoutes**](/windows/desktop/api/Routprot/nc-routprot-pdo_update_routes)

[*DoUpdateServices*](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))

[**GetEventMessage**](/windows/desktop/api/Routprot/nc-routprot-pget_event_message)

[**GetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_global_info)

[**GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info)

[**GetMfeStatus**](/windows/desktop/api/Routprot/nc-routprot-pget_mfe_status)

[**GetNeighbors**](/windows/desktop/api/Routprot/nc-routprot-pget_neighbors)

[**InterfaceStatus**](/windows/desktop/api/Routprot/nc-routprot-pinterface_status)

[**MibCreate**](/windows/desktop/api/Routprot/nc-routprot-pmib_create)

[**MibDelete**](/windows/desktop/api/Routprot/nc-routprot-pmib_delete)

[**MibGet**](/windows/desktop/api/Routprot/nc-routprot-pmib_get)

[**MibGetFirst**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_first)

[**MibGetNext**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_next)

[*MibGetTrapInfo*](/windows/desktop/api/Routprot/nc-routprot-pmib_get_trap_info)

[**MibSet**](/windows/desktop/api/Routprot/nc-routprot-pmib_set)

[**MibSetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_set_trap_info)

[**QueryPower**](/windows/desktop/api/Routprot/nc-routprot-pquery_power)

[**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)

[**SetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_global_info)

[**SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info)

[**SetPower**](/windows/desktop/api/Routprot/nc-routprot-pset_power)

[**StartComplete**](/windows/desktop/api/Routprot/nc-routprot-pstart_complete)

[**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol)

[**StopProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstop_protocol)

[**UnbindInterface**](/previous-versions/windows/desktop/legacy/aa382296(v=vs.85))

Si le protocole de routage prend en charge la gestion des services, implémentez la fonction suivante en plus des éléments listés ci-dessus :

[**DoUpdateServices**](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))

 

 