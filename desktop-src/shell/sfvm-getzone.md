---
description: 'Permet à l’objet de rappel de fournir des informations sur la zone Internet. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
ms.assetid: 6fae7925-b1be-4270-9318-7fa517563dad
title: Message SFVM_GETZONE (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 946823f1081a8cc3e01c917e424e3bdd41861f85b0abe0cad654ea09c296f8fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118048428"
---
# <a name="sfvm_getzone-message"></a>\_Message SFVM GETZONE

\[cette notification est prise en charge par Windows XP Service Pack 2 (SP2) et Windows Server 2003. Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures de Windows.\]

Permet à l’objet de rappel de fournir des informations sur la zone Internet. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETZONE
    lParam = (LPARAM)(DWORD*) zone;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*zone* \[ à\]
</dt> <dd>

L’une des valeurs suivantes indiquant la zone Internet. Ces valeurs constituent l’énumération [**URLZONE**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) , définie dans urlmon. h.

<dt>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**\_ordinateur local \_ URLZONE**


</dt> <dd>

Zone utilisée pour le contenu qui se trouve déjà sur l’ordinateur local de l’utilisateur. Cette zone n’est pas exposée par l’interface utilisateur.

</dd> <dt>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**\_Intranet URLZONE**


</dt> <dd>

Zone utilisée pour le contenu trouvé sur un intranet.

</dd> <dt>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE \_ approuvé**


</dt> <dd>

Zone utilisée pour les sites Web de confiance sur Internet.

</dd> <dt>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**URLZONE \_ Internet**


</dt> <dd>

Zone utilisée pour la majeure partie du contenu sur Internet.

</dd> <dt>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE \_ non approuvé**


</dt> <dd>

Zone utilisée pour les sites Web qui ne sont pas approuvés.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
