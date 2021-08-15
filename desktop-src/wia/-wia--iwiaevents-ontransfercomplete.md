---
description: Événement qui se produit lorsqu’un transfert de données est effectué avec succès.
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: Événement WIA. OnTransferComplete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnTransferComplete
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 9095302a2f3fe75e1939ebb979ec4aad4d87b0462a5b40997e5523e7313d98e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209273"
---
# <a name="wiaontransfercomplete-event"></a>Événement WIA. OnTransferComplete

Événement qui se produit lorsqu’un transfert de données est effectué avec succès.

## <a name="syntax"></a>Syntaxe


```JScript
Wia.OnTransferComplete(
  Item,
  Path
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Item* 
</dt> <dd>

Objet [**Item**](-wia-item.md) transféré.

</dd> <dt>

*Chemin d’accès* 
</dt> <dd>

Chemin d’accès et nom de fichier de l’image transférée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

WIA notifie le script ou l’application lorsqu’un transfert de données, une image ou un son se termine correctement. Implémentez la sous-routine **objWia** \_ **OnTransferComplete ()** pour autoriser votre script ou votre application à répondre à l’achèvement du transfert de données.

Par exemple, vous souhaiterez peut-être qu’un script affiche une image après son transfert.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




