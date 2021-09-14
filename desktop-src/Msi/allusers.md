---
Description: La propriété ALLUSERS configure le contexte d’installation du package.
ms.assetid: 942e7764-a80f-4880-9559-72174f1827f7
title: ALLUSERS, propriété
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: f4e490216a16b6ef36cdb90efebbbf24a7b1b9cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092722"
---
# <a name="allusers-property"></a>ALLUSERS, propriété

La propriété **ALLUSERS** configure le contexte d’installation du package. l’Windows Installer effectue une installation par utilisateur ou une installation par ordinateur en fonction des privilèges d’accès de l’utilisateur, si des privilèges élevés sont requis pour installer l’application, la valeur de la propriété **ALLUSERS** , la valeur de la propriété [**MSIINSTALLPERUSER**](msiinstallperuser.md) et la version du système d’exploitation.

La valeur de la propriété **ALLUSERS** , au moment de l’installation, détermine le [contexte d’installation](installation-context.md).

-   La valeur 1 de la propriété **ALLUSERS** spécifie le contexte d’installation par ordinateur.
-   Une valeur de propriété **ALLUSERS** d’une chaîne vide ("") spécifie le contexte d’installation par utilisateur.
-   si la valeur de la propriété **allusers** est définie sur 2, la Windows Installer rétablit toujours la valeur 1 pour la propriété **allusers** et effectue une installation par ordinateur ou réinitialise la valeur de la propriété **allusers** sur une chaîne vide ("") et effectue une installation par utilisateur. La valeur ALLUSERS = 2 permet au système de réinitialiser la valeur de **ALLUSERS** et le contexte d’installation, en fonction des privilèges de l’utilisateur et de la version de Windows.

    **Windows 7 :** Affectez à la propriété **ALLUSERS** la valeur 2 pour utiliser la propriété [**MSIINSTALLPERUSER**](msiinstallperuser.md) afin de spécifier le contexte d’installation. Définissez la propriété **MSIINSTALLPERUSER** sur une chaîne vide ("") pour une installation par ordinateur. Affectez la valeur 1 à la propriété **MSIINSTALLPERUSER** pour une installation par utilisateur. Si le package a été écrit conformément aux instructions de développement décrites dans [création de package unique](single-package-authoring.md), les utilisateurs disposant d’un accès utilisateur peuvent installer dans le contexte par utilisateur sans avoir à fournir des informations d’identification UAC. Si l’utilisateur dispose de privilèges d’accès d’utilisateur, le programme d’installation effectue une installation par ordinateur uniquement si les informations d’identification d’administrateur sont fournies à la boîte de dialogue UAC.

    **Windows Vista :** affectez à la propriété **ALLUSERS** la valeur 2 et Windows Installer est conforme au [*contrôle de compte d’utilisateur*](u-gly.md) (UAC). Si l’utilisateur dispose de privilèges d’accès utilisateur et ALLUSERS = 2, le programme d’installation effectue une installation par ordinateur uniquement si les informations d’identification d’administrateur sont fournies à la boîte de dialogue UAC. Si le contrôle de compte d’utilisateur est activé et que les informations d’identification d’administrateur appropriées ne sont pas fournies, l’installation échoue avec une erreur indiquant que des privilèges d’administrateur sont nécessaires. Si le contrôle de compte d’utilisateur est désactivé par la clé de Registre, la stratégie de groupe ou le panneau de configuration, la boîte de dialogue contrôle de compte d’utilisateur ne s’affiche pas et l’installation échoue avec une erreur indiquant que des privilèges d’administrateur sont requis.

    **Windows XP :** affectez à la propriété **ALLUSERS** la valeur 2 et Windows Installer effectue une installation par utilisateur si l’utilisateur dispose de privilèges d’accès utilisateur.

-   si la valeur de la propriété **ALLUSERS** n’est pas égale à 2, le Windows Installer ignore la valeur de la propriété [**MSIINSTALLPERUSER**](msiinstallperuser.md) .

## <a name="example"></a>Exemple

```xml
  <!-- Disallow user from installing for all users -->
    <Property Id="ALLUSERS" Secure="yes"/>
    <Condition Message="Setting the ALLUSERS property is not allowed because [ProductName] is a per-user application. Setup will now exit.">
      NOT ALLUSERS
    </Condition>
```

exemple de [Windows exemples classiques](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) sur GitHub.

## <a name="default-value"></a>Valeur par défaut

Le contexte d’installation par défaut recommandé est par utilisateur. Si **ALLUSERS** n’est pas défini, le programme d’installation effectue une installation par utilisateur. Vous pouvez vous assurer que la propriété **ALLUSERS** n’a pas été définie en définissant sa valeur sur une chaîne vide (""), ALLUSERS = "".

## <a name="remarks"></a>Notes

Le [contexte d’installation](installation-context.md) détermine les valeurs des propriétés [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**startupfolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)et [**CommonFiles64Folder**](commonfiles64folder.md) . Le contexte d’installation détermine les parties du registre où les entrées de la [table du Registre](registry-table.md) et de la [table RemoveRegistry](removeregistry-table.md), avec-1 dans la colonne racine, sont écrites ou supprimées.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[**MSIINSTALLPERUSER**](msiinstallperuser.md)
</dt> <dt>

[Contexte d’installation](installation-context.md)
</dt> <dt>

[Création d’un package unique](single-package-authoring.md)
</dt> </dl>

 

 




