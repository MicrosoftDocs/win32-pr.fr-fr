---
description: La méthode CollectUserInfo de l’objet installer appelle une séquence de l’Assistant interface utilisateur qui collecte et stocke les informations utilisateur et le code du produit.
ms.assetid: 2faacf38-1af1-4e8a-a3f6-87733104614e
title: Installer. CollectUserInfo, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CollectUserInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 255f9c5bfbd9f7ed476314e8ac1c9ed58568c083b8f6ea7704bbe5cfef15b769
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632916"
---
# <a name="installercollectuserinfo-method"></a>Installer. CollectUserInfo, méthode

La méthode **CollectUserInfo** de l’objet [**installer**](installer-object.md) appelle une séquence de l’Assistant interface utilisateur qui collecte et stocke les informations utilisateur et le code du produit.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.CollectUserInfo(
  Product
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Produit* 
</dt> <dd>

Spécifie le [**Code de produit**](productcode.md) du produit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Une application doit appeler la méthode **CollectUserInfo** la première fois qu’elle est exécutée. La méthode **CollectUserInfo** ouvre le package d’installation du produit et appelle une séquence créée de l’Assistant de l’interface utilisateur qui collecte les informations utilisateur. À la fin de la séquence de l’Assistant, les informations utilisateur collectées sont enregistrées. La propriété [**UILevel**](installer-uilevel.md) doit être définie sur msiUILevelFull, car cette API requiert une interface utilisateur créée.

La méthode **CollectUserInfo** appelle la [boîte de dialogue firstrun](firstrun-dialog.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
</dt> </dl>

 

 




