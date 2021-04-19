---
description: Cette rubrique décrit les instructions de programmation pour localiser les chaînes de Registre redirigées. Pour plus d’informations, consultez Utilisation de la redirection de chaîne de registre.
ms.assetid: 03d1512f-35a6-4b3a-9a0e-97e17bd9b126
title: Recherche de chaînes redirigées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f11600ad57c04de54d914c2c876b67967dfa1467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514249"
---
# <a name="locating-redirected-strings"></a>Recherche de chaînes redirigées

Cette rubrique décrit les instructions de programmation pour localiser les chaînes de Registre redirigées. Pour plus d’informations, consultez [utilisation de la redirection de chaîne de Registre](using-registry-string-redirection.md).

## <a name="load-a-language-neutral-registry-value"></a>Charger une valeur de Registre Language-Neutral

Sur Windows Vista et versions ultérieures, l’application MUI utilise une valeur de Registre indépendante du langage pour autoriser l’accès aux chaînes spécifiques à la langue stockées dans une table de ressources de type chaîne. Pour plus d’informations, consultez créer une ressource Language-Neutral dans [utilisation de la redirection de chaînes de Registre](using-registry-string-redirection.md).

Le code d’application qui lit la valeur neutre dans le langage du registre doit charger les chaînes dans la langue d’interface utilisateur appropriée en appelant [**RegLoadMUIStringW**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa). Si vous utilisez cette fonction, votre application n’a pas à gérer explicitement le chargement des ressources.

Si vous mettez à jour une application existante à l’aide de la langue indépendante du Registre, vous conservez généralement les valeurs de chaîne existantes, localisées en anglais ou dans une autre langue dans le registre, comme des secours et une compatibilité descendante. Le fait de conserver une chaîne littérale dans le registre permet à l’application de revenir à la chaîne littérale en cas d’échec d’un appel à [**RegLoadMUIStringW**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa) . Vous devez décider comment implémenter ce type de secours, car MUI n’offre aucune prise en charge pour une telle implémentation.

## <a name="use-shell-api-to-set-shortcut-strings-from-the-registry"></a>Utiliser l’API Shell pour définir des chaînes de raccourci à partir du Registre

Votre application peut utiliser l’API Shell pour créer des chaînes pour les raccourcis qui lient des fichiers ou des dossiers dans le menu **Démarrer** ou sur le bureau. Pour plus d’informations, consultez créer des ressources pour les chaînes de raccourci dans [utilisation de la redirection de chaînes de Registre](using-registry-string-redirection.md).

L’application peut utiliser [**SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) pour charger le nom complet compatible MUI pour un raccourci. Elle doit utiliser [**IShellLink :: SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) pour définir l’info-bulle associée. Les appels inscrivent les chaînes avec le registre. Prenons les exemples suivants, pour lesquels « HKCR » représente la \_ clé de \_ Registre racine de classes HKEY :


```C++
HKCR,"CLSID\%CLSID_AntiSpyware%",,,"Windows AntiSpyware"

HKCR,"CLSID\%CLSID_AntiSpyware%","LocalizedString",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-104"

HKCR,"CLSID\%CLSID_AntiSpyware%","InfoTip",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-208"
```



La première ligne fournit une chaîne littérale non localisée pour la compatibilité descendante et de secours. La deuxième ligne montre la méthode compatible MUI pour inscrire le nom complet. Cette ligne indique l’identificateur de chaîne 104 stocké dans Msascui.exe (pour Windows XP) ou dans son fichier spécifique à la langue (pour Windows Vista). Cet identificateur de chaîne correspond à « Favoris réseau ». La troisième ligne de l’exemple gère l’inscription de l’info-bulle. % CLSID \_ antispyware% spécifie une variable d’environnement représentant le GUID qui correspond à l’identificateur de classe de ce composant.

Pour l’exemple ci-dessus, l’application appelle [**SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) pour spécifier le chemin d’accès de l’exécutable pour les deux premiers paramètres, et spécifie *idsRes* comme « @% ProgramFiles% \\ Windows AntiSpyware \\MSASCui.exe, 104 ». Un appel à [**IShellLink :: SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription), spécifie le chemin d’accès de l’info-bulle sous la forme « @% ProgramFiles% \\ Windows AntiSpyware \\MSASCui.exe, 208 ».

## <a name="query-friendly-document-type-names-in-the-registry"></a>Rechercher dans le registre des noms de type de document conviviaux

La création de ressources pour les noms de type de document convivial est décrite dans créer des ressources pour des noms de type de document conviviaux dans [à l’aide de la redirection de chaîne de Registre](using-registry-string-redirection.md). Pour interroger un nom de document convivial, l’application doit utiliser [**IQueryAssociations :: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init), suivi d’un appel à [**IQueryAssociations :: GetString**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-getstring). L’appel à **IQueryAssociations :: init** spécifie le type de document, par exemple « . txt ». L’appel à **IQueryAssociations :: GetString** doit spécifier ASSOCSTR \_ FRIENDLYDOCNAME comme identificateur de chaîne.

## <a name="register-microsoft-management-console-snap-in-strings-not-read-from-the-registry"></a>Inscrire les chaînes du composant logiciel enfichable Microsoft Management Console non lues dans le registre

Votre application peut utiliser un composant logiciel enfichable MMC (Microsoft Management Console) pour héberger ses tâches de gestion. La plupart des chaînes sont gérées en tant que ressources à l’aide des paramètres du registre décrits dans créer des ressources de type chaîne pour Microsoft Management Console Snap-Ins dans utilisation de la [redirection de chaînes de Registre](using-registry-string-redirection.md). Toutefois, certains composants logiciels enfichables inscrivent les valeurs de chaîne de registre que MMC ne peut pas lire à partir du Registre. Dans ce cas, le composant logiciel enfichable doit obtenir les valeurs à l’aide de l’interface [**ISnapinAbout**](/windows/win32/api/mmc/nn-mmc-isnapinabout) , qui est compatible avec mui.

## <a name="set-the-display-name-and-description-for-a-windows-service-from-the-registry"></a>Définir le nom complet et la description d’un service Windows à partir du Registre

Si votre application MUI utilise un service Windows, elle doit afficher le nom et la description de l’affichage du service. Les ressources associées sont présentées dans la section « créer des ressources de type chaîne pour un service Windows » de la rubrique [utilisation de la redirection de chaînes de Registre](using-registry-string-redirection.md).

Pour définir le nom d’affichage du service, l’application MUI appelle [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) ou [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga). Le nom est une chaîne au format " `@<PE-path>,-<stringID>[;<comment>]` ". Par exemple, si votre service est implémenté par un fichier. dll avec le chemin d’accès% ProgramFiles% \\ % myPath% \\MyDll.dll et que l’identificateur de chaîne du nom complet propre à la langue est 347, le paramètre est spécifié comme « `@%ProgramFiles%\\%MyPath%\\MyDll.dll,-347` ». Les doubles barres obliques inverses ( \\ \\ ) sont nécessaires, car C/C++ utilise la barre oblique inverse comme caractère d’échappement dans les chaînes.

Pour définir la description du service spécifique à une langue, l’application MUI doit faire en sorte que le membre **lpDescription** d’une structure de [**\_ Description de service**](/windows/win32/api/winsvc/ns-winsvc-service_descriptiona) indique une chaîne de forme « `@<PE-path>,-<stringID>[;<comment>]` », en référençant l’identificateur de chaîne approprié. L’application appelle ensuite [**ChangeServiceConfig2**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a) avec le paramètre *dwInfoLevel* spécifié en tant que \_ \_ Description de la configuration du service et le paramètre *lpInfo* spécifié en tant que structure de **\_ Description du service** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche de ressources Win32 PE](locating-win32-pe-resources.md)
</dt> <dt>

[Utilisation de la redirection de chaînes de Registre](using-registry-string-redirection.md)
</dt> </dl>

 

 
