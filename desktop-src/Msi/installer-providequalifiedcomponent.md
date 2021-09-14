---
description: La méthode ProvideQualifiedComponent de l’objet installer retourne le chemin d’accès complet au composant et effectue toute installation nécessaire. Si nécessaire, cette méthode vous invite à entrer la source et incrémente le nombre d’utilisations de la fonctionnalité.
ms.assetid: 4f9a5094-1556-4d86-8b51-c8c3ce1cbed4
title: Installer. ProvideQualifiedComponent, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideQualifiedComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 73c830610b49976e3625dd333c57f39e43d4be14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012101"
---
# <a name="installerprovidequalifiedcomponent-method"></a>Installer. ProvideQualifiedComponent, méthode

La méthode **ProvideQualifiedComponent** de l’objet [**installer**](installer-object.md) retourne le chemin d’accès complet au composant et effectue toute installation nécessaire. Si nécessaire, cette méthode vous invite à entrer la source et incrémente le nombre d’utilisations de la fonctionnalité.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.ProvideQualifiedComponent(
  Category,
  Qualifier,
  InstallMode
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Catégorie* 
</dt> <dd>

Spécifie l’ID de composant pour le composant demandé. Ce n’est peut-être pas le GUID du composant lui-même, mais plutôt un serveur qui fournit les fonctionnalités correctes, comme dans la colonne ComponentId de la [table PublishComponent](publishcomponent-table.md).

</dd> <dt>

*Qualificateur* 
</dt> <dd>

Spécifie un qualificateur dans une liste de composants de publicité (à partir de la [table PublishComponent](publishcomponent-table.md)).

</dd> <dt>

*InstallMode* 
</dt> <dd>

Définit le mode d’installation. Ce paramètre peut avoir l’une des valeurs indiquées dans le tableau suivant.



| InstallMode                                                                                                                                                                                                                                                                                                                                                         | Signification                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                 | Fournit le composant, en effectuant toutes les installations nécessaires.<br/>                                                                                                                                                           |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>– 1</dt> </dl>                                                                            | Fournit le composant uniquement si la fonctionnalité existe ; Sinon, retourne une chaîne vide. Ce mode vérifie l’existence du fichier de clé du composant.<br/>                                                                      |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>– 2</dt> </dl>                                                                | Fournit le composant uniquement si la fonctionnalité existe ; Sinon, retourne une chaîne vide. Ce mode vérifie uniquement que le composant est inscrit, mais ne vérifie pas l’existence du fichier de clé du composant.<br/>              |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>– 3</dt> </dl>                                    | Fournit le chemin d’accès du composant uniquement si la fonctionnalité existe avec un paramètre InstallState de *msiInstallStateLocal*. Cela vérifie l’inscription du composant, mais ne vérifie pas l’existence du fichier de clé du composant.<br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <dt>**combinaison des indicateurs msiReinstallMode**</dt> <dt></dt> </dl> | Appelle [**ReinstallFeature**](installer-reinstallfeature.md) pour réinstaller la fonctionnalité à l’aide de ce paramètre pour le paramètre *ReinstallMode* , puis fournit le composant.<br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
</dt> </dl>

 

 




