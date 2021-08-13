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
ms.openlocfilehash: f16cc37556d217a217b814b5ce87cb705cd3105d4a8c2ad3f503d617aeda2cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633037"
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

 

 




