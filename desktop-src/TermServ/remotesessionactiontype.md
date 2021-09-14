---
title: Énumération RemoteSessionActionType
description: Utilisé pour spécifier le type d’action à distance.
ms.assetid: C0DA0FA2-6FE0-4B40-B169-4592A1BE2AD6
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’énumération RemoteSessionActionType
topic_type:
- apiref
api_name:
- RemoteSessionActionType
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 291bb9fdd2cadfef3881bc27a47f9fc1bb1bce68
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324573"
---
# <a name="remotesessionactiontype-enumeration"></a>Énumération RemoteSessionActionType

Utilisé pour spécifier le type d’action à distance.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _RemoteSessionActionType { 
  RemoteSessionActionCharms        = 0,
  RemoteSessionActionAppbar        = 1,
  RemoteSessionActionSnap          = 2,
  RemoteSessionActionStartScreen   = 3,
  RemoteSessionActionAppSwitch     = 4,
  RemoteSessionActionActionCenter  = 4
} RemoteSessionActionType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**RemoteSessionActionCharms**
</dt> <dd>

Affiche les icônes dans la session à distance.

</dd> <dt>

<span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**RemoteSessionActionAppbar**
</dt> <dd>

Affiche la barre de l’application dans la session à distance.

</dd> <dt>

<span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**RemoteSessionActionSnap**
</dt> <dd>

Ancre l’application dans la session à distance. Cette option est dépréciée et ne doit pas être utilisée.

</dd> <dt>

<span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**RemoteSessionActionStartScreen**
</dt> <dd>

Provoque l’affichage de l’écran de démarrage dans la session à distance.

</dd> <dt>

<span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**RemoteSessionActionAppSwitch**
</dt> <dd>

Provoque l’affichage de la fenêtre de changement d’application dans la session à distance. C’est le même que l’utilisateur qui appuie sur Alt + Tab.

</dd> <dt>

<span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**RemoteSessionActionActionCenter**
</dt> <dd>

Entraîne l’affichage du centre de maintenance dans la session à distance. C’est le même que l’utilisateur qui appuie sur Win + A.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012 et Windows 8 :** cette valeur n’est pas prise en charge avant Windows Server 2016 et Windows 10.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient8::SendRemoteAction**](imsrdpclient8-sendremoteaction.md)
</dt> </dl>

 

 





