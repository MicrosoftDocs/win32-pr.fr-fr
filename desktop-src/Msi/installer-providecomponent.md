---
description: La méthode ProvideComponent de l’objet installer retourne le chemin d’accès complet au composant et effectue toute installation nécessaire.
ms.assetid: 2bf09515-6f65-4712-89c1-01c43c1ce27c
title: Installer. ProvideComponent, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e383c532d496ed217bdb7743b8171d732d61b2d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012100"
---
# <a name="installerprovidecomponent-method"></a>Installer. ProvideComponent, méthode

La méthode **ProvideComponent** de l’objet [**installer**](installer-object.md) retourne le chemin d’accès complet au composant et effectue toute installation nécessaire. Si nécessaire, la méthode **ProvideComponent** de l’objet [**installer**](installer-object.md) demande la source et incrémente le nombre d’utilisations de la fonctionnalité.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.ProvideComponent(
  Product,
  Feature,
  Component,
  InstallMode
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Produit* 
</dt> <dd>

Spécifie le code de produit du produit.

</dd> <dt>

*Fonctionnalité* 
</dt> <dd>

Spécifie l’ID de fonctionnalité de la fonctionnalité qui contient le composant.

</dd> <dt>

*Composant* 
</dt> <dd>

Spécifie le code du composant.

</dd> <dt>

*InstallMode* 
</dt> <dd>

Définit le mode d’installation. Ce paramètre peut avoir l’une des valeurs indiquées dans le tableau suivant.



| Nom                                                                                                                                                                                                                                                                                                                                                               | Signification                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                | Fournit le chemin d’accès du composant, en effectuant n’importe quelle installation, si nécessaire.<br/>                                                                                                                                                  |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>– 1</dt> </dl>                                                                           | Fournit le chemin d’accès du composant uniquement si la fonctionnalité existe ; Sinon, retourne une chaîne vide. Ce mode vérifie l’existence du fichier de clé du composant.<br/>                                                                |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>– 2</dt> </dl>                                                               | Fournit le chemin d’accès du composant uniquement si la fonctionnalité existe. Sinon, retourne une chaîne vide. Ce mode vérifie l’inscription du composant, mais ne vérifie pas l’existence du fichier de clé du composant.<br/>                 |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>– 3</dt> </dl>                                   | Fournit le chemin d’accès du composant uniquement si la fonctionnalité existe avec un paramètre InstallState de *msiInstallStateLocal*. Cela vérifie l’inscription du composant, mais ne vérifie pas l’existence du fichier de clé du composant.<br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <dt>**combinaison des indicateurs msiReinstallMode**</dt><dt></dt> </dl> | Appelle [**ReinstallFeature**](installer-reinstallfeature.md) pour réinstaller la fonctionnalité à l’aide de ce paramètre pour le paramètre *ReinstallMode* , puis fournit le composant.<br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La méthode **ProvideComponent** combine les fonctionnalités de [**UseFeature**](installer-usefeature.md), [**ConfigureFeature**](installer-configurefeature.md)et [**ComponentPath**](installer-componentpath.md). La méthode **ProvideComponent** simplifie la séquence d’appel, mais incrémente également le nombre d’utilisations et doit être utilisée avec précaution afin d’éviter des nombres d’utilisations inexacts. La méthode **ProvideComponent** offre également moins de flexibilité qu’une série d’appels individuels aux méthodes et propriétés mentionnées précédemment.

Si l’application est en cours de récupération à la suite d’une situation inattendue, l’application a probablement déjà appelé [**UseFeature**](installer-usefeature.md) et incrémenté le nombre d’utilisations. Dans ce cas, l’application doit éviter d’incrémenter le nombre d’utilisations en appelant la méthode [**ConfigureFeature**](installer-configurefeature.md) au lieu de la méthode **ProvideComponent** .

L’option msiInstallModeExisting ne peut pas être utilisée en association avec les indicateurs msiReinstallMode.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
</dt> </dl>

 

 




