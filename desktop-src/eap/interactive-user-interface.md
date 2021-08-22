---
title: Interface utilisateur interactive
description: Le fournisseur qui implémente le protocole d’authentification peut également fournir une interface utilisateur interactive pour le protocole.
ms.assetid: 4f8ba0a4-3b52-4e7c-9e67-748f8d81d7a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811f35ac3492e45e80721f800925a003edbb8116ac8c199a1b633e08a28de675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117779"
---
# <a name="interactive-user-interface"></a>Interface utilisateur interactive

Le fournisseur qui implémente le protocole d’authentification peut également fournir une interface utilisateur interactive pour le protocole. L’interface utilisateur interactive permet au protocole d’authentification d’obtenir des informations supplémentaires de la part de l’utilisateur en fonction des besoins au cours de la session d’authentification.

L’interface utilisateur interactive peut être implémentée dans la même DLL que le protocole d’authentification ou dans une DLL distincte. En outre, la DLL qui implémente l’interface utilisateur interactive peut prendre en charge plusieurs protocoles d’authentification. Le chemin d’accès à la DLL de l’interface utilisateur interactive est stocké dans la valeur de Registre [RAS \_ \_ \_ INTERACTIVEUI valueName](authentication-protocol-registry-values.md) , sous la clé du protocole d’authentification. Pour plus d’informations sur la création de cette valeur de Registre, consultez la page [installation d’EAP](eap-installation.md).

La DLL de l’interface utilisateur interactive doit exporter des points d’entrée pour les fonctions suivantes :<dl>

[**RasEapInvokeInteractiveUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui)  
[**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)  
</dl>

L’interface utilisateur interactive doit prendre en charge les messages de [**\_ commande WM**](../menurc/wm-command.md) où [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) est égal à IDCANCEL.

Pour afficher l’interface utilisateur interactive, le protocole d’authentification doit affecter la **valeur true** au membre **fInvokeInteractiveUI** de la structure de [**\_ \_ sortie EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) . Le protocole d’authentification peut éventuellement définir les membres **pUIContextData** et **dwSizeOfUIContextData** sur **true** . Le service d’authentification utilise les valeurs de ces membres pour passer des données de contexte à l’interface utilisateur interactive. Le protocole d’authentification retourne la structure de **\_ \_ sortie EAP PPP** en tant que paramètre dans la fonction [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) .

Le service d’authentification appelle l’interface utilisateur interactive en appelant [**RasEapInvokeInteractiveUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui). Le service transmet ensuite au protocole d’authentification un pointeur vers les données retournées par l’interface utilisateur interactive lors de l’appel suivant à [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)). Le pointeur est passé en tant que membre d’une structure [**\_ \_ d’entrée EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) . Une fois **RasEapMakeMessage** retourné, le service appelle [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) pour libérer la mémoire occupée par les informations. Par conséquent, le protocole d’authentification doit copier les informations dans une mémoire tampon de mémoire privée pendant l’appel à **RasEapMakeMessage**.

 

 