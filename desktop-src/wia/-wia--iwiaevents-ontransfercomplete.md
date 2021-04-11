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
ms.openlocfilehash: d33685e0e8fe233f96e9841359e56f759032d17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202897"
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

## <a name="remarks"></a>Notes

WIA notifie le script ou l’application lorsqu’un transfert de données, une image ou un son se termine correctement. Implémentez la sous-routine **objWia** \_ **OnTransferComplete ()** pour autoriser votre script ou votre application à répondre à l’achèvement du transfert de données.

Par exemple, vous souhaiterez peut-être qu’un script affiche une image après son transfert.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




