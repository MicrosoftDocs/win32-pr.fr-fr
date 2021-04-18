---
description: Le stockage de chaînes codées en dur dans le registre fait partie d’un modèle de localisation antérieur à Windows Vista.
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: Utilisation de la redirection de chaînes de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f6e1420aae0ff41c386e19852bebbd1a322c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523058"
---
# <a name="using-registry-string-redirection"></a>Utilisation de la redirection de chaînes de Registre

Le stockage de chaînes codées en dur dans le registre fait partie d’un modèle de localisation antérieur à Windows Vista. Elle n’est pas prise en charge par MUI. Dans le modèle actuel, l’interface utilisateur du système d’exploitation s’exécute dans des fichiers de ressources spécifiques à une langue, en plus d’une base indépendante du langage. Les composants du système d’exploitation utilisent le registre de manière indépendante de la langue.

MUI utilise uniquement les chaînes de Registre redirigées définies par les ressources Win32 PE dans le fichier de ressources de langue de base. La redirection est définie séparément, par exemple dans un fichier. inf. Ce type de stockage permet au chargeur de ressources de sélectionner automatiquement les ressources de langue appropriées lors du chargement du module de ressources.

> [!Note]  
> Cette rubrique se rapporte uniquement aux ressources Win32 PE. Si vous utilisez des ressources PE non Win32, vous devez fournir une redirection de chaîne de Registre personnalisée, si nécessaire.

 

## <a name="create-a-language-neutral-resource"></a>Créer une ressource Language-Neutral

Une application MUI s’exécutant sur Windows Vista et versions ultérieures utilise une ressource de chaîne indépendante du langage pour autoriser l’accès aux chaînes spécifiques à la langue stockées dans une table de ressources de type chaîne. Le code d’application qui lit ces valeurs à partir du Registre est décrit dans la section chargement d’un Language-Neutral valeur de registre de [localisation des chaînes redirigées](locating-redirected-strings.md).

Les données d’une valeur de Registre indépendante du langage ont le format « `@<PE-path>,-<stringID>[;<comment>]` », où :

-   *PE-Path* spécifie le chemin d’accès de l’exécutable. Vous pouvez spécifier le chemin d’accès à l’aide d’une variable d’environnement, telle que% ProgramFiles%, pour prendre en charge le déploiement. Pour faire référence à votre chaîne, vous pouvez également conserver les informations de chemin d’accès au fichier. Dans ce cas, votre application doit avoir des moyens, par exemple, une autre valeur de Registre, pour communiquer son propre répertoire d’installation.
-   *stringID* spécifie l’identificateur de ressource numérique de la ressource de chaîne appropriée, qui est implémentée comme n’importe quelle autre ressource de chaîne localisable.
-   le *Commentaire* spécifie des informations facultatives pour le débogage ou la lisibilité de la valeur de registre. Les fonctions de l’API du Registre ignorent le commentaire lors du chargement de la chaîne.

> [!Note]  
> Les données de la valeur de registre ne font pas de référence explicite au fichier de ressources spécifique au langage. Le fichier approprié est déterminé au moment de l’exécution, en fonction des préférences de langue de l’interface utilisateur actuelle.

 

Une valeur de Registre est entrée sans espace entre les valeurs « , » et « - ». Une valeur de Registre correcte est :

`shell32.dll,-22912`

Une valeur de Registre incorrecte est :

`shell32.dll, -22912`

Un exemple de Windows Vista est la valeur de Registre avec les données suivantes :

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a>Créer des ressources pour les chaînes de raccourci

Lorsque l’application MUI affiche son nom dans l’interface utilisateur de l’interpréteur de commandes, une chaîne d’info-bulle s’affiche pour l’icône de l’application. Vous devez créer des ressources de type chaîne pour le nom d’affichage de votre application et la chaîne d’info-bulle associée pour chaque langue prise en charge. Lorsque les ressources sont prêtes, votre application peut utiliser les chaînes comme décrit dans la section utiliser l’API Shell pour charger des chaînes de raccourci à partir du registre de [localisation des chaînes redirigées](locating-redirected-strings.md).

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a>Préparer les ressources pour un raccourci créé avec Windows Installer

Si vous utilisez Windows Installer (MSI) pour créer un raccourci, les ressources de type chaîne incluent le nom complet et la description du raccourci. Dans la [table de raccourcis MSI](../msi/shortcut-table.md), la dll de ressource est référencée dans les colonnes appropriées et les identificateurs de ressource pour le nom complet et la description de votre raccourci sont utilisés dans les colonnes correspondantes de l’identificateur de ressource.

Pour que le raccourci de l’application fonctionne correctement avec la technologie de ressources MUI, gardez les points suivants à l’esprit lors de la préparation des chaînes de raccourci :

-   Utilisez des variables d’environnement ou un chemin d’accès relatif pour inscrire la DLL. Vous pouvez spécifier @% systemroot% \\ system32 \\shell32.dll tant que le type de chaîne de Registre est reg \_ expand \_ sz. L’identificateur de ressource de chaîne pour « document texte » dans Shell32.dll est 12345.
-   N’utilisez pas d’espaces autour des symboles « , » et « - ». Un exemple correct est « shell32.dll,-22912 ».
-   N’utilisez pas de nom de fichier courts. Ce type de nom ne fonctionne pas avec le chargeur de ressources.

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a>Préparer des ressources pour un raccourci à l’aide du format INF

Si vous utilisez le format de fichier INF pour créer des chaînes de raccourci, le fichier de ressources doit apporter les paramètres de registre suivants. Ces instructions supposent l’utilisation de la syntaxe ProfileItems de l’API d’installation.

1.  Modifiez la valeur de l’info-bulle pour pointer vers la référence de redirection de chaînes à l’aide du chemin d’accès et de l’identificateur de ressource.
2.  Ajoutez la nouvelle valeur DisplayResource sous les sections installation de ProfileItems.

Voici un exemple qui illustre l’ajout de l’application Calculatrice au menu **Démarrer** :


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



Utilisez la syntaxe indiquée ci-dessous lorsque vous utilisez INF pour ajouter des éléments, par exemple, un dossier de groupe d’accès, au menu **Démarrer** . Cette syntaxe suppose l’utilisation de la \[ \] prise en charge de StartMenuItems par le programme d’installation, similaire à la syntaxe utilisée dans syssetup. inf.


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



Définissez la valeur *info-bulle* sur la référence de chaîne « `@<path>,-resID` ».

Le nom d’affichage est déterminé par les valeurs *resDLL* et *resID* . La valeur *resID* spécifie l’identificateur de ressource pour une ressource de type chaîne associée au fichier indépendant de la langue. La valeur *resDLL* spécifie le chemin d’accès au fichier indépendant du langage.

## <a name="create-resources-for-friendly-document-type-names"></a>Créer des ressources pour les noms de type de document conviviaux

Vous devez implémenter des chaînes nom convivial et info-bulle pour votre application en tant que ressources de type chaîne. Pour permettre aux noms de type de document conviviaux de réagir à la langue de l’interface utilisateur, l’application doit inscrire les noms à l’aide de la valeur FriendlyTypeName sous la clé de l’identificateur de programme pour le type de fichier. La valeur par défaut de la clé d’identificateur de programme doit être conservée pour assurer la compatibilité descendante. Pour plus d’informations sur l’accès aux noms à partir de votre application, consultez la section relative aux noms de types de document conviviaux dans le registre de [localisation des chaînes redirigées](locating-redirected-strings.md).

Le travail spécifique implique les étapes suivantes :

1.  Implémentez les chaînes nom convivial et info-bulle en tant que ressources de chaîne spécifiques au langage.
2.  Ajoutez la valeur FriendlyTypeName sous la clé de Registre type de document. Les données de la valeur suivent le modèle « `@<path>,-<resID>` », où *chemin d’accès* indique l’exécutable et *resID* est l’identificateur de ressource d’une ressource de type chaîne localisable associée à cet exécutable.
3.  Spécifiez la valeur de registre d’info-bulle en fonction du format « `@<path>,-<resID>` ».

L’exemple suivant montre les paramètres de registre d’un fichier. txt :


```C++
HKCR\.txt
@="txtfile"
"Content Type"="text/plain"

HKCR\txtfile
@="Text Document"

"FriendlyTypeName" = "@%systemroot%\system32\shell32.dll,-12345"

"InfoTip" = "@%systemroot%\system32\shell32.dll,-12346"
```



## <a name="provide-resources-for-shell-verb-action-strings"></a>Fournir des ressources pour les chaînes d’action de verbe de Shell

Les chaînes d’action de certains verbes, par exemple « ouvrir » et « modifier », sont affichées dans le menu contextuel qui s’affiche lorsque l’utilisateur clique avec le bouton droit sur un fichier dans l’Explorateur Windows. Votre application n’a pas besoin de spécifier des chaînes pour les verbes d’interpréteur de commandes courants, car l’interpréteur de commandes possède ses propres valeurs par défaut compatibles MUI pour ces verbes. Toutefois, vous devez fournir des ressources de type chaîne localisables pour les chaînes qui représentent des verbes rares.

Sur les systèmes d’exploitation antérieurs à Windows XP, les chaînes pour les verbes de Shell dans le Registre sont restituées à l’aide de la syntaxe suivante, où *verb* spécifie le nom de verbe réel :


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



Voici un exemple :


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



Sur Windows XP et versions ultérieures, vous pouvez utiliser un niveau d’indirection pour que la chaîne d’action dépende de la langue de l’interface utilisateur. Ces systèmes d’exploitation prennent en charge une valeur MUIVerb pour la définition d’une chaîne compatible MUI. Voici un exemple d’entrée de Registre pour un verbe rare :


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
"MUIVerb" = "@%systemroot%\system32\sample.exe,-9875"
```



Votre application MUI doit également être en mesure d’enregistrer l’ancienne valeur par défaut en tant que chaîne localisable, comme indiqué ci-dessous :


```C++
HKCR\Sample.app\shell\Disc
@ = "@%systemroot%\system32\sample.exe,-9875"
```



> [!Note]  
> L’inscription de l’ancienne valeur par défaut n’est pas recommandée, car elle nécessite une installation différente sur Windows XP et versions ultérieures à partir de la configuration utilisée sur les systèmes d’exploitation antérieurs.

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a>Créer des ressources pour les chaînes Verb, Protocol et AuxUserType

Vous devez créer des ressources de type chaîne localisables pour les chaînes Verb, Protocol et AuxUserType. Utilisez les paramètres de registre suivants :


```C++
HKCR\CLSID\{<Your_CLSID>}\Verb\<number> @="<Your Verb>, <menu_flag>, <verb_flag>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...

HKCR\CLSID\{<Your_CLSID>}\AuxUserType\<number>
@="<Your Short Name>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID1"
...

HKCR\<Your_Name>\protocol\StdFileEditing\verb\<number>
@="<Your Verb>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...
```



La valeur spécifiée pour LocalizedString contient ou remplace uniquement la valeur de *votre verbe*, pas les deux valeurs d’indicateur.

Voici un résumé pour vous aider à vérifier les paramètres de registre appropriés :

-   Si CLSID a une \\ \\ clé Insertable de HKCR CLSID {CLSID} \\ , définissez la valeur de CLSID par défaut à l’aide de HKCR \\ CLSID \\ {CLSID} \\ LocalizedString.
-   Si CLSID contient une ou plusieurs sous-clés sous \\ le \\ verbe HKCR CLSID {CLSID} \\ , définissez chaque chaîne de verbe individuelle à l’aide du \\ verbe HKCR CLSID \\ {CLSID} \\ \\ \\ LocalizedString.
-   Si CLSID contient une ou plusieurs sous-clés sous le \\ verbe Stdfileediting du protocole HKCR {ProgID} \\ \\ \\ , définissez chaque chaîne de verbe individuelle à l’aide du \\ verbe Stdfileediting du protocole HKCR {ProgID} \\ \\ \\ \\ \\ LocalizedString.
-   Si CLSID contient une ou plusieurs sous-clés AuxUserType listées sous HKCR \\ CLSID \\ {CLSID} \\ AuxUserType, définissez chaque entrée AuxUserType à l’aide de HKCR \\ CLSID \\ {CLSID} \\ AuxUserType \\ xxx \\ LocalizedString.

## <a name="create-a-resource-for-the-uninstall-program"></a>Créer une ressource pour le programme de désinstallation

Pour inscrire le programme de désinstallation de l’application, vous pouvez créer des valeurs de Registre dans la sous-clé de l’identificateur unique de l’application sous la clé de Registre HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Uninstall. Les valeurs à définir sont les suivantes : DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, contact, Comments, DisplayIcon, README, UrlUpdateInfo.

> [!Note]  
> Pour activer la technologie MUI pour chaque valeur, vous pouvez ajouter « \_ Localized » au nom de la valeur.

 

Les composants du système d’exploitation sont requis pour fournir une valeur pour DisplayName \_ localisée de manière spécifique à MUI. Vous devez placer le nom complet dans une DLL, par exemple Res.dll, en tant que ressource de type chaîne, en supposant que l’identificateur soit 1245. L’application peut ensuite enregistrer le nom complet comme DisplayName \_ localisé avec la valeur « @ \\res.DLL,-1245 ». Tous les autres paramètres du Registre doivent être conservés tels quels, y compris la valeur d’origine de DisplayName.

## <a name="create-resources-for-sound-events"></a>Créer des ressources pour les événements sonores

Windows associe certains événements à des fichiers son, par exemple, un événement de notification de courrier ou un événement d’alarme de batterie critique. Les noms des événements doivent être affichés par l’interface utilisateur et doivent prendre en charge la globalisation. Par conséquent, vous devez implémenter une ressource de type chaîne localisable pour la description de chaque description d’événement. Ajoutez une nouvelle valeur de Registre pour chaque nom d’événement, en plus de la valeur par défaut codée en dur.

Pour activer un événement sonore, procédez comme suit :

1.  Implémentez la description en tant que ressource de chaîne localisable.
2.  Ajoutez une nouvelle valeur de Registre pour le nom complet, en plus de la valeur par défaut codée en dur. La disposition du registre associée est indiquée ci-dessous :


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



Si l’interpréteur de commandes ne peut pas trouver ou récupérer la valeur de DispFileName, il utilise la description par défaut.

## <a name="create-resources-for-keyboard-layout-strings"></a>Créer des ressources pour les chaînes de disposition du clavier

Si votre application implémente une disposition de clavier, elle requiert une ressource de chaîne localisable pour le nom de la disposition pour l’affichage à l’écran, par exemple, dans les listes de dispositions de clavier. Chaque disposition de clavier a une clé de Registre sous HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ layouts.

Parmi les valeurs de cette clé figurent le texte de disposition, un nom explicite pour la compatibilité descendante et le nom d’affichage de la disposition. Les données fournies pour le nom complet de la disposition doivent être une référence de chaîne sous la forme « `@<path>,-resID` », qui fait référence à une ressource de chaîne localisable associée à la disposition du clavier.

Voici un exemple de paramètre de Registre pour la disposition de clavier espagnol (Espagne) :

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a>Représenter les chaînes de boîte de dialogue commune d’objet OLE Insert

Vous pouvez implémenter le nom complet d’un objet OLE pouvant être inséré en tant que ressource de chaîne localisable associée au code qui implémente cet objet. La [boîte de dialogue OLE Insert Object](/cpp/mfc/reference/coleinsertdialog-class) obtient un nom complet à partir de la clé de Registre HKCR \\ CLSID \\ { *<GUID>* }, où *GUID* identifie l’identificateur de classe d’un objet OLE à insérer. Windows Vista et versions ultérieures implémentent ce type d’objet de façon localisable, à l’aide d’un nom d’affichage compatible avec MUI qui permet la personnalisation de la langue de l’interface utilisateur. En revanche, les systèmes d’exploitation antérieurs à Windows Vista implémentent le nom complet de ce type d’objet à l’aide de la valeur par défaut de la clé de Registre correspondante. En général, il s’agit d’un nom anglais (États-Unis) ou d’un nom dans la langue de l’interface utilisateur par défaut du système.

> [!Note]  
> Tous les objets qui correspondent aux sous-clés de la clé de registre ne peuvent pas être insérés.

 

La valeur par défaut de la \\ clé HKCR CLSID \\ { *<GUID>* } doit conserver un nom explicite pour la compatibilité descendante. Toutefois, il doit également définir la valeur LocalizedString, au format « `@<path>,-ResID` », où Path identifie le fichier exécutable qui implémente l’objet. La valeur ResID spécifie l’identificateur de ressource de la chaîne localisable pour le nom complet.

Par exemple, le script d’inscription de l’objet clip Media pouvant être inséré contient les lignes suivantes :


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



La première ligne fournit une compatibilité descendante en plaçant une chaîne de texte simple dans le Registre sous la forme d’un nom d’affichage par défaut. La deuxième ligne fournit l’accès au nom complet compatible MUI. Elle indique l’identificateur de chaîne stocké dans Mplay32.exe. La chaîne avec l’identificateur 9217 dans Mplay32.exe peut être associée à des valeurs de ressource de type chaîne pour un nombre quelconque de langues. Son nom anglais (États-Unis) est « clip multimédia ».

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a>Créer des ressources de type chaîne pour Microsoft Management Console Snap-Ins

Vous devez créer une ressource de type chaîne localisable pour chaque composant logiciel enfichable MMC (Microsoft Management Console) utilisé par votre application MUI. Comme un composant logiciel enfichable fait partie d’une console, il dispose d’une interface utilisateur et doit être globalisé pour fonctionner dans plusieurs langues.

La plupart du temps, les composants logiciels enfichables MMC génèrent les mêmes problèmes de globalisation et de localisation que l’application MUI elle-même. Un composant logiciel enfichable MMC doit refléter son nom dans le registre pour l’affichage. L’entrée de registre doit inclure à la fois une référence indirecte à une ressource de chaîne localisable et une chaîne littérale pour la compatibilité descendante.

Chaque composant logiciel enfichable MMC possède une clé de Registre sous HKEY \_ local \_ machine \\ Software \\ Microsoft \\ MMC \\ composants logiciels enfichables. Parmi les valeurs de cette clé, citons NameString, en spécifiant un nom explicite pour la compatibilité descendante, et NameStringIndirect, en spécifiant une référence indirecte à une ressource de type chaîne localisable. Pour NameStringIndirect, vous devez fournir une référence de chaîne sous la forme « `@<path>,-resID` », représentant une ressource de chaîne localisable.

Par exemple, vous pouvez définir le paramètre suivant pour Mymmc.dll, où 12345 est l’identificateur de la ressource de chaîne correspondante contenant le nom localisable du composant logiciel enfichable :


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



Certains composants logiciels enfichables inscrivent d’autres valeurs de chaîne de registre que MMC ne lit pas à partir du Registre. Pour plus d’informations sur l’utilisation de ces valeurs, consultez inscrire la console de gestion Microsoft Snap-In chaînes non lues dans le registre dans [localisation de chaînes redirigées](locating-redirected-strings.md).

## <a name="create-string-resources-for-a-windows-service"></a>Créer des ressources de type chaîne pour un service Windows

Bien qu’un service Windows ait généralement peu ou pas d’interface utilisateur, il doit afficher un nom compatible MUI et fournit généralement une description spécifique à une langue compatible MUI. La clé de Registre qui décrit un service Windows prend en charge uniquement la valeur DisplayName pour le nom du service et la valeur Description pour la description du service.

Les paramètres du service Windows sont créés à partir de l’application, comme décrit dans définir le nom complet et la description d’un service Windows à partir du Registre dans [localisation des chaînes redirigées](locating-redirected-strings.md). Si votre application ne définit pas les valeurs de Registre pour l’interface utilisateur du service, les valeurs du Registre restent définies sur l’anglais, même si l’interface utilisateur est dans une autre langue.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Préparation des ressources](preparing-resources.md)
</dt> <dt>

[Recherche de chaînes redirigées](locating-redirected-strings.md)
</dt> </dl>

 

 
