---
description: SFVM \_ GETPANE peut être modifié ou non disponible.
ms.assetid: 9621b921-e97f-4219-953a-7c961a81c379
title: Message SFVM_GETPANE (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2800be1b7b427e13014686e587b51fc4bf7d7617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952334"
---
# <a name="sfvm_getpane-message"></a>\_Message SFVM GETPANE

\[**SFVM \_ GETPANE** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

Permet à l’objet de rappel de fournir le volet de barre d’État dans lequel afficher les informations de la zone Internet. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETPANE
    wParam = (WPARAM)(int) paneID;
    lParam = (LPARAM)(DWORD*) pane;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*paneID* \[ dans\]
</dt> <dd>

ID du volet demandé. Il s’agit normalement \_ de la zone de volet, mais peut prendre l’une des valeurs suivantes.

<dt>

<span id="PANE_NONE"></span><span id="pane_none"></span>

<span id="PANE_NONE"></span><span id="pane_none"></span>**VOLET \_ aucun**


</dt> <dd>

Aucun volet.

</dd> <dt>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>**ZONE de volet \_**


</dt> <dd>

Volet zone Internet.

</dd> <dt>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**VOLET \_ hors connexion**


</dt> <dd>

Volet hors connexion.

</dd> <dt>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>**imprimante du volet \_**


</dt> <dd>

Le volet d’indication d’impression.

</dd> <dt>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>**SSL de volet \_**


</dt> <dd>

Le volet SSL.

</dd> <dt>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**NAVIGATION dans les VOLETs \_**


</dt> <dd>

Volet de navigation.

</dd> <dt>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**progression du volet \_**


</dt> <dd>

Volet de la barre de progression.

</dd> <dt>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**confidentialité du volet \_**


</dt> <dd>

Volet de l’indicateur de confidentialité.

</dd> </dl> </dd> <dt>

*volet* \[ à\]
</dt> <dd>

Pointeur vers une **valeur DWORD** contenant le numéro du volet.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                |
| Fin de la prise en charge des clients<br/>    | Windows XP SP2<br/>                                                      |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
