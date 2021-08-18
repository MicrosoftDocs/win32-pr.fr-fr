---
description: Les fonctions de Registre sont les suivantes.
ms.assetid: a490b748-42e8-462b-9a7f-a8b21438ea79
title: Fonctions du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81f5aff4dad00691f606911c1cf092933aa121eaf7a2d25aacbcc8a83948b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885212"
---
# <a name="registry-functions"></a>Fonctions du Registre

Les fonctions de Registre sont les suivantes.



| Fonction                                                           | Description                                                                                                                                    |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)           | Récupère la taille actuelle du Registre et la taille maximale que le Registre est autorisé à atteindre sur le système.                          |
| [**Échec RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey)                                 | Ferme un handle vers la clé de Registre spécifiée.                                                                                                 |
| [**RegConnectRegistry**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya)                   | Établit une connexion à un handle de Registre prédéfini sur un autre ordinateur.                                                                  |
| [**RegCopyTree**](/windows/desktop/api/Winreg/nf-winreg-regcopytreea)                                 | Copie la clé de Registre spécifiée, ainsi que ses valeurs et sous-clés, dans la clé de destination spécifiée.                                        |
| [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa)                           | Crée la clé de Registre spécifiée.                                                                                                            |
| [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda)           | Crée la clé de Registre spécifiée et l’associe à une transaction.                                                                       |
| [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya)                               | Supprime une sous-clé et ses valeurs.                                                                                                               |
| [**RegDeleteKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeyexa)                           | Supprime une sous-clé et ses valeurs de la vue spécifique à la plateforme spécifiée du Registre.                                                     |
| [**RegDeleteKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeytransacteda)           | Supprime une sous-clé et ses valeurs de la vue spécifique à la plateforme spécifiée du registre en tant qu’opération traitée.                           |
| [**RegDeleteKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeyvaluea)                     | Supprime la valeur spécifiée de la clé de Registre et de la sous-clé spécifiées.                                                                        |
| [**RegDeleteTree**](/windows/desktop/api/Winreg/nf-winreg-regdeletetreea)                             | Supprime les sous-clés et les valeurs de la clé spécifiée de manière récursive.                                                                               |
| [**RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea)                           | Supprime une valeur nommée de la clé de Registre spécifiée.                                                                                         |
| [**RegDisablePredefinedCache**](/windows/desktop/api/Winreg/nf-winreg-regdisablepredefinedcache)     | Désactive la mise en cache des handles pour le handle de Registre prédéfini pour **HKEY \_ Current \_ User** pour le processus en cours.                                |
| [**RegDisablePredefinedCacheEx**](/windows/desktop/api/Winreg/nf-winreg-regdisablepredefinedcacheex) | Désactive la mise en cache des handles pour tous les descripteurs de Registre prédéfinis pour le processus en cours.                                                           |
| [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey)         | Désactive la réflexion du Registre pour la clé spécifiée.                                                                                            |
| [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey)           | Active la réflexion du Registre pour la clé désactivée spécifiée.                                                                                    |
| [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa)                               | Énumère les sous-clés de la clé de Registre ouverte spécifiée.                                                                                     |
| [**RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea)                               | Énumère les valeurs de la clé de Registre ouverte spécifiée.                                                                                     |
| [**Regflushkey a**](/windows/desktop/api/Winreg/nf-winreg-regflushkey)                                 | Écrit tous les attributs de la clé de Registre ouverte spécifiée dans le registre.                                                                    |
| [**RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity)                | Récupère une copie du descripteur de sécurité protégeant la clé de Registre ouverte spécifiée.                                                        |
| [**RegGetValue**](/windows/desktop/api/Winreg/nf-winreg-reggetvaluea)                                 | Récupère le type et les données pour la valeur de Registre spécifiée.                                                                                  |
| [**RegLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya)                                   | Crée une sous-clé sous **HKEY \_ Users** ou **HKEY \_ local \_ machine** et stocke les informations d’inscription d’un fichier spécifié dans cette sous-clé. |
| [**RegLoadMUIString**](/windows/desktop/api/Winreg/nf-winreg-regloadmuistringa)                       | Charge la chaîne spécifiée à partir de la clé et de la sous-clé spécifiées.                                                                                  |
| [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue)         | Notifie l’appelant des modifications apportées aux attributs ou au contenu d’une clé de Registre spécifiée.                                                   |
| [**RegOpenCurrentUser**](/windows/desktop/api/Winreg/nf-winreg-regopencurrentuser)                   | Récupère un handle vers la clé de l' **\_ \_ utilisateur actuel HKEY** pour l’utilisateur que le thread actuel emprunte.                                        |
| [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa)                               | Ouvre la clé de Registre spécifiée.                                                                                                              |
| [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda)               | Ouvre la clé de Registre spécifiée et l’associe à une transaction.                                                                         |
| [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot)           | Récupère un handle vers la clé **\_ \_ racine HKEY classes** pour l’utilisateur spécifié.                                                                  |
| [**RegOverridePredefKey**](/windows/desktop/api/Winreg/nf-winreg-regoverridepredefkey)               | Cartes une clé de registre prédéfinie à une clé de registre spécifiée.                                                                                    |
| [**RegQueryInfoKey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya)                         | Récupère des informations sur la clé de Registre spécifiée.                                                                                        |
| [**RegQueryMultipleValues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa)           | Récupère le type et les données pour une liste de noms de valeurs associés à une clé de Registre ouverte.                                                    |
| [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey)             | Détermine si la réflexion a été désactivée ou activée pour la clé spécifiée.                                                              |
| [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa)                         | Récupère le type et les données pour un nom de valeur spécifié associé à une clé de Registre ouverte.                                                   |
| [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)                             | Remplace le fichier qui stocke une clé de Registre et toutes ses sous-clés par un autre fichier.                                                                |
| [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya)                             | Lit les informations de Registre dans un fichier spécifié et les copie sur la clé spécifiée.                                                       |
| [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya)                                   | Enregistre la clé spécifiée et toutes ses sous-clés et valeurs dans un nouveau fichier.                                                                       |
| [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa)                               | Enregistre la clé spécifiée et toutes ses sous-clés et valeurs dans un nouveau fichier. Vous pouvez spécifier le format de la clé ou de la ruche enregistrée.                 |
| [**RegSetKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regsetkeyvaluea)                           | Définit les données pour la valeur spécifiée dans la clé de Registre et la sous-clé spécifiées.                                                                |
| [**RegSetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-regsetkeysecurity)                | Définit la sécurité d’une clé de Registre ouverte.                                                                                                     |
| [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa)                             | Définit les données et le type d’une valeur spécifiée sous une clé de registre.                                                                              |
| [**RegUnLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya)                               | Décharge la clé de Registre spécifiée et ses sous-clés du Registre.                                                                          |



 

Les fonctions Shell suivantes peuvent être utilisées avec le registre :

-   [**AssocCreate**](/windows/desktop/api/shlwapi/nf-shlwapi-assoccreate)
-   [**AssocQueryKey**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerykeya)
-   [**AssocQueryString**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringa)
-   [**AssocQueryStringByKey**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringbykeya)
-   [**SHCopyKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shcopykeya)
-   [**SHDeleteEmptyKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeleteemptykeya)
-   [**SHDeleteKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeletekeya)
-   [**SHDeleteValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeletevaluea)
-   [**SHEnumKeyEx**](/windows/desktop/api/shlwapi/nf-shlwapi-shenumkeyexa)
-   [**SHEnumValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shenumvaluea)
-   [**SHGetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shgetvaluea)
-   [**SHQueryInfoKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shqueryinfokeya)
-   [**SHQueryValueEx**](/windows/desktop/api/shlwapi/nf-shlwapi-shqueryvalueexa)
-   [**SHRegCloseUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregcloseuskey)
-   [**SHRegCreateUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregcreateuskeya)
-   [**SHRegDeleteEmptyUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregdeleteemptyuskeya)
-   [**SHRegDeleteUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregdeleteusvaluea)
-   [**SHRegDuplicateHKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregduplicatehkey)
-   [**SHRegEnumUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregenumuskeya)
-   [**SHRegEnumUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregenumusvaluea)
-   [**SHRegGetBoolUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetboolusvaluea)
-   [**SHRegGetIntW**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetintw)
-   [**SHRegGetPath**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetpatha)
-   [**SHRegGetUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetusvaluea)
-   [**SHRegOpenUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregopenuskeya)
-   [**SHRegQueryInfoUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregqueryinfouskeya)
-   [**SHRegQueryUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregqueryusvaluea)
-   [**SHRegSetPath**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetpatha)
-   [**SHRegSetUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetusvaluea)
-   [**SHRegWriteUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregwriteusvaluea)
-   [**SHSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shsetvaluea)

Les fonctions de fichier d’initialisation sont les suivantes. Ils récupèrent les informations de et copient les informations dans un fichier d’initialisation défini par le système ou par l’application. Ces fonctions sont fournies uniquement à des fins de compatibilité avec les versions 16 bits de Windows. Les nouvelles applications doivent utiliser le registre.



| Fonction                                                               | Description                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**GetPrivateProfileInt**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofileint)                   | Récupère un entier associé à une clé dans la section spécifiée d’un fichier d’initialisation.     |
| [**GetPrivateProfileSection**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilesection)           | Récupère toutes les clés et valeurs de la section spécifiée d’un fichier d’initialisation.             |
| [**GetPrivateProfileSectionNames**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilesectionnames) | Récupère les noms de toutes les sections d’un fichier d’initialisation.                                     |
| [**GetPrivateProfileString**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilestring)             | Récupère une chaîne à partir de la section spécifiée dans un fichier d’initialisation.                           |
| [**GetPrivateProfileStruct**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilestruct)             | Récupère les données associées à une clé dans la section spécifiée d’un fichier d’initialisation.       |
| [**GetProfileInt**](/windows/desktop/api/Winbase/nf-winbase-getprofileinta)                                 | Récupère un entier d’une clé dans la section spécifiée du fichier Win.ini.                      |
| [**GetProfileSection**](/windows/desktop/api/Winbase/nf-winbase-getprofilesectiona)                         | Récupère toutes les clés et valeurs de la section spécifiée du fichier Win.ini.                   |
| [**GetProfileString**](/windows/desktop/api/Winbase/nf-winbase-getprofilestringa)                           | Récupère la chaîne associée à une clé dans la section spécifiée du fichier Win.ini.           |
| [**WritePrivateProfileSection**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilesectiona)       | Remplace les clés et les valeurs de la section spécifiée dans un fichier d’initialisation.                  |
| [**WritePrivateProfileString**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilestringa)         | Copie une chaîne dans la section spécifiée d’un fichier d’initialisation.                              |
| [**WritePrivateProfileStruct**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilestructa)         | Copie des données dans une clé de la section spécifiée d’un fichier d’initialisation.                         |
| [**WriteProfileSection**](/windows/desktop/api/Winbase/nf-winbase-writeprofilesectiona)                     | Remplace le contenu de la section spécifiée dans le fichier Win.ini par les valeurs et clés spécifiées. |
| [**WriteProfileString**](/windows/desktop/api/Winbase/nf-winbase-writeprofilestringa)                       | Copie une chaîne dans la section spécifiée du fichier Win.ini.                                    |



 

## <a name="obsolete-functions"></a>Fonctions obsolètes

Ces fonctions sont fournies uniquement à des fins de compatibilité avec les versions 16 bits de Windows :

-   [**RegCreateKey**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeya)
-   [**RegEnumKey**](/windows/desktop/api/Winreg/nf-winreg-regenumkeya)
-   [**RegOpenKey**](/windows/desktop/api/Winreg/nf-winreg-regopenkeya)
-   [**RegQueryValue**](/windows/desktop/api/Winreg/nf-winreg-regqueryvaluea)
-   [**RegSetValue**](/windows/desktop/api/Winreg/nf-winreg-regsetvaluea)

 

 
