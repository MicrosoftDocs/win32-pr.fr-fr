---
description: la méthode ForceSourceListResolution de l’objet Installer force l’Windows Installer à rechercher dans la liste source une source de produit valide.
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: Installer. ForceSourceListResolution, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ForceSourceListResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cafff03a392fc1977fd19b5b8415ca499d614c2c4ba3fb4f7104edd5344f3a86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630591"
---
# <a name="installerforcesourcelistresolution-method"></a>Installer. ForceSourceListResolution, méthode

La méthode **ForceSourceListResolution** de l’objet [**installer**](installer-object.md) oblige le programme d’installation à rechercher dans la liste source une source de produit valide la prochaine fois qu’une source est nécessaire, par exemple quand le programme d’installation effectue une installation ou une réinstallation, ou lorsqu’il a besoin du chemin d’accès d’un jeu de composants à exécuter à partir de la source.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.ForceSourceListResolution(
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

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Résilience source](source-resiliency.md)
</dt> </dl>

 

 




