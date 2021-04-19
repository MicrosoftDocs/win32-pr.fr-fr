---
description: La méthode ClearSourceList de l’objet installer supprime toutes les sources réseau de la liste source.
ms.assetid: a4e4beb2-a4d7-48e7-9c8d-dd1ae19fe92a
title: Installer. ClearSourceList, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClearSourceList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f9468775c75533b766a160a390410908d04bf6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542536"
---
# <a name="installerclearsourcelist-method"></a>Installer. ClearSourceList, méthode

La méthode **ClearSourceList** de l’objet [**installer**](installer-object.md) supprime toutes les sources réseau de la liste source.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.ClearSourceList(
  Product,
  User
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Produit* 
</dt> <dd>

Spécifie le code du produit.

</dd> <dt>

*Utilisateur* 
</dt> <dd>

Nom d’utilisateur pour l’installation par utilisateur ; chaîne null ou vide pour une installation par ordinateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiSourceListClearAll**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)
</dt> <dt>

[Résilience source](source-resiliency.md)
</dt> </dl>

 

 




