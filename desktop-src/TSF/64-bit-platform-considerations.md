---
title: 64-considérations sur les bits
description: Avec la disponibilité accrue de Windows 64 bits, les utilisateurs attendent des méthodes d’entrée, telles que des claviers internationaux dans différents langages ou éditeurs de méthode d’entrée (IME) dans les langues d’Extrême-Orient, pour fonctionner correctement avec les applications 32 bits et 64 bits.
ms.assetid: 6a99ad45-202c-4fbb-9707-341bc9fde21e
keywords:
- Text Services Framework (TSF), Windows 64 bits
- TSF (Text Services Framework), Windows 64 bits
- services de texte, Windows 64 bits
- Windows 64 bits
- Text Services Framework (TSF), éditeur de méthode d’entrée (IME)
- TSF (Text Services Framework), éditeur de méthode d’entrée (IME)
- services de texte, éditeur de méthode d’entrée (IME)
- Éditeur de méthode d'entrée (IME)
- IME (éditeur de méthode d’entrée)
- Text Services Framework (TSF), claviers internationaux
- TSF (Text Services Framework), claviers internationaux
- services de texte, claviers internationaux
- claviers internationaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045ec699c7a433f15b92467e3072d30acbf01936
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382121"
---
# <a name="64-bit-considerations"></a>64-considérations sur les bits

Avec la disponibilité accrue de Windows 64 bits, les utilisateurs attendent des méthodes d’entrée, telles que des claviers internationaux dans différents langages ou éditeurs de méthode d’entrée (IME) dans les langues d’Extrême-Orient, pour fonctionner correctement avec les applications 32 bits et 64 bits. Lors du développement de composants de méthode d’entrée ou de services de texte pour Microsoft Windows, il est important de considérer Windows 64 bits comme une plateforme cible potentielle pour votre produit.

Étant donné que les éditeurs de contenu et les services de texte (basés sur l’infrastructure de services de texte) sont généralement implémentés en tant que bibliothèques de liens dynamiques (dll), il est important de noter que les dll sont générées spécifiquement pour une utilisation dans des environnements 32 bits ou des environnements 64 bits. une DLL générée pour une utilisation dans des environnements 32 bits ne peut pas être utilisée par les applications 64 bits, et inversement.

> [!Note]  
> WOW64 n’atténue pas cette restriction de DLL spécifique à un bit. Pour plus d’informations sur WOW64, consultez [exécution d’Applications 32 bits](/windows/desktop/WinProg64/running-32-bit-applications).

 

Cette rubrique aborde les considérations de conception importantes pour le développement d’éditeurs et de services de texte pour une utilisation sur Windows 64 bits.

## <a name="64-bit-considerations-for-imes"></a>64-points à prendre en considération pour les IME

Cette section décrit les considérations spéciales impliquées dans la création d’IME pour une utilisation avec Windows 64 bits. Pour plus d’informations sur les éditeurs de [méthode d’entrée, consultez Éditeur de méthode d’entrée](/previous-versions/windows/desktop/dnacc/input-method-editor-and-text-services-framework-accessibility).

## <a name="building-32-bit-and-64-bit-versions-of-an-ime"></a>Génération de versions 32 bits et 64 bits d’un IME

En raison du problème de compatibilité 32 bits/64 bits précédemment mentionné avec les dll, certaines précautions doivent être prises pour s’assurer que les éditeurs IME fonctionnent de manière transparente avec n’importe quelle application (32 bits ou 64 bits) exécutée sous Windows 64 bits. La solution recommandée pour permettre à votre IME de fonctionner de manière transparente avec les applications 32 bits et 64 bits sur une plateforme 64 bits consiste à créer et à installer des versions parallèles 32 bits et 64 bits de la DLL IME. En règle générale, les développeurs génèrent des dll parallèles à partir d’une source unique en ajustant les paramètres de plateforme cible dans leur environnement de génération. Pour plus d’informations sur les applications 32 bits et 64 bits à source unique, consultez se [préparer pour Windows 64 bits](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows).

## <a name="side-by-side-installation-of-64-bit-and-32-bit-input-method-editors"></a>Installation côte à côte des éditeurs de méthode d’entrée 64 bits et 32 bits

Les développeurs d’IME et de services de texte doivent connaître les considérations 64 bits décrites dans cette rubrique. Heureusement, les utilisateurs finaux de ces services n’ont pas à se préoccuper de ces détails spécifiques à l’implémentation. Une fonctionnalité de Windows 64 bits est la possibilité de masquer les versions spécifiques à 64 bits et 32 bits des dll IME des utilisateurs finaux. Lorsque les deux versions de l’IME sont correctement installées côte à côte, Windows 64 bits reconnaît la présence des versions 64 bits et 32 bits de l’IME et présente ces éditeurs IME spécifiques à l’utilisateur final comme un IME *logique* unique. Lorsqu’un utilisateur final doit utiliser un IME, Windows 64 bits choisit en toute transparence la version de l’IME (32 bits ou 64 bits) appropriée pour les circonstances données.

Pour que les installations côte à côte des IME 64 bits et 32 bits fonctionnent correctement (autrement dit, pour représenter les deux dll propres à la plateforme comme un IME logique unique à l’utilisateur), les conditions suivantes doivent être remplies :

-   Les développeurs doivent créer des versions spécifiques à la plateforme (une pour Windows 32 bits et une pour Windows 64 bits) de la DLL IME.
-   Les dll 32 bits et 64 bits doivent partager le même nom de fichier.
-   La configuration requise pour le répertoire d’installation doit être suivie. Pour plus d’informations, consultez Configuration requise pour le répertoire d’installation.

Les installations côte à côte des dll IME 32 bits et 64 bits partagent la même clé de Registre pour le stockage des données de configuration (y compris le nom du fichier DLL) :


```C++
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layouts
```



La fonction [**ImmInstallIME**](/windows/desktop/api/imm/nf-imm-imminstallimea) est utilisée pour créer cette clé de registre. Le programme d’installation et d’installation d’un IME doit appeler cette fonction pour inscrire l’IME en tant que disposition de clavier prise en charge. La fonction **ImmInstallIME** ne doit être appelée qu’une seule fois, que ce soit à partir de la version 32 bits ou 64 bits de la dll IME.

## <a name="mismatched-ime-dlls"></a>Dll IME non appariées

L’installation de la version 32 bits d’un IME sur Windows 64 bits n’est ni recommandée ni prise en charge. Si une application 64 bits tente de charger un IME 32 bits, l’IME échoue en silence quand l’application tente de charger la disposition de clavier associée.

> [!IMPORTANT]
>
> Aucune boîte de dialogue d’avertissement ou message ne s’affiche lorsqu’une application 64 bits/une erreur de conflit IME 32 bits se produit.

 

64-points à prendre en compte pour les services de texte

Cette section décrit les considérations spéciales impliquées dans la création de services de texte pour une utilisation dans les environnements 64 bits. Pour plus d’informations sur les services de texte et l’infrastructure de services de texte, consultez [Text Services Framework](text-services-framework.md).

## <a name="building-32-bit-and-64-bit-text-services"></a>Génération de services de texte 32 bits et 64 bits

Un service de texte est implémenté en tant qu’objet COM (Component Object Model) exposé sur une DLL. Par conséquent, des conflits de DLL 32 bits/64 bits peuvent se produire avec les services de texte installés sur Windows 64 bits. Tout comme avec les éditeurs IME, la solution recommandée pour permettre à votre service de texte de fonctionner de manière transparente avec les applications 32 bits et 64 bits sur une plateforme 64 bits consiste à créer et à installer des versions parallèles 32 bits et 64 bits de la DLL du service de texte.

## <a name="side-by-side-installation-of-64-bit-and-32-bit-text-services"></a>Installation côte à côte de services de texte 64 bits et 32 bits

Pour une version 32 bits et une version 64 bits d’un service de texte à installer côte à côte et représentées à l’utilisateur sous la forme d’un service de texte logique unique, les conditions suivantes doivent être remplies :

-   Les deux versions du service de texte spécifient le même identificateur de classe (CLSID) lorsqu’elles sont inscrites auprès du sous-système COM.
-   Les deux versions du service de texte sont inscrites indépendamment. Pour plus d’informations, consultez [inscription d’applications com](/windows/desktop/com/registering-com-applications).

Quand un service de texte 32 bits est inscrit avec Windows 64 bits, l’opération d’inscription est redirigée de façon transparente vers la clé de Registre suivante :


```C++
HKEY_CLASS_ROOT\Wow6432Node\CLSID
```



[Redirecteur du Registre](/windows/desktop/WinProg64/registry-redirector)


```C++
HKEY_LOCAL_MACHINE\Software\Microsoft\CTF\TIP
```



[](/windows/desktop/api/Msctf/nn-msctf-itfinputprocessorprofiles)[Inscription du service de texte](text-service-registration.md) ITfInputProcessorProfiles

La version 64 bits et la version 32 bits d’un service de texte peuvent être en cours d’utilisation simultanément. Dans les cas où les deux versions d’un service de texte doivent manipuler des objets partagés, la coordination des objets partagés d’accès doit être conçue dans le service de texte. Chaque service de texte est responsable de la gestion des objets partagés qui sont utilisés ou nécessaires.

## <a name="installing-only-32-bit-text-services-on-64-bit-windows"></a>Installation des services de texte 32 bits sur Windows 64 bits

L’installation de la version 32 bits d’un service de texte sur une plate-forme Windows 64 bits n’est ni recommandée ni prise en charge. En raison du mappage d’inscription effectué sur les plateformes Windows 64 bits, une application 64 bits peut énumérer les services d’un service de texte de 32 bits par le biais de l’interface **ITfInputProcessorProfiles** . Toutefois, si une application 64 bits tente de charger un service de texte 32 bits, le chargement échoue en silence.

> [!IMPORTANT]
>
> Aucune boîte de dialogue d’avertissement ou message ne s’affiche lorsqu’une erreur de conflit de service de texte 32 bits ou une application 64 bits se produit.

 

Autres considérations

## <a name="installation-directory-requirements"></a>Configuration requise pour le répertoire d’installation

Cette section décrit la configuration requise pour l’installation des fichiers binaires IME et de services texte. Si ces exigences ne sont pas respectées, votre service de texte ou IME risque de ne pas fonctionner correctement.

**Dll IME**

Sur les plateformes Windows 64 bits, installez les dll IME 32 bits et 64 bits dans les répertoires suivants :

-   Installer des dll IME 32 bits dans le répertoire système SysWOW64 ; Appelez [**GetSystemWow64Directory**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directorya)ou [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) avec **CSIDL \_ SYSTEMX86** pour récupérer ce chemin d’accès au répertoire. Sinon, si vous utilisez [Windows Installer](/windows/desktop/Msi/about-windows-installer), utilisez la propriété [**SystemFolder**](/windows/desktop/Msi/systemfolder) .
-   Installer des dll IME 64 bits dans le répertoire système system32 ; Appelez [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)ou **SHGetFolderPath** avec le [ \_ système CSIDL](/windows/desktop/shell/csidl) pour récupérer ce chemin d’accès au répertoire. Ou, pour Windows Installer, utilisez la propriété [**System64Folder**](/windows/desktop/Msi/system64folder) .

**Dll du service de texte et fichiers binaires associés**

Sur les plateformes Windows 64 bits, installez les dll du service de texte 32 bits et 64 bits, ainsi que tous les autres fichiers binaires associés à votre service de texte ou à votre IME, dans les répertoires suivants :

-   Installez les dll du service de texte 32 bits et tout autre fichier binaire 32 bits dans un sous-répertoire du répertoire Program Files (x86); Appelez **SHGetFolderPath** avec **le \_ programme CSIDL \_ FILESX86** pour récupérer ce chemin d’accès au répertoire. Ou, pour Windows Installer, utilisez la propriété [**ProgramFilesFolder**](/windows/desktop/Msi/programfilesfolder) .
-   Installez les dll du service de texte 64 bits et tout autre fichier binaire 64 bits dans un sous-répertoire du répertoire Program Files. Appelez **SHGetFolderPath** avec **les \_ \_ fichiers programme CSIDL** pour récupérer ce chemin d’accès au répertoire. Ou, pour Windows Installer, utilisez la propriété [**ProgramFiles64Folder**](/windows/desktop/Msi/programfiles64folder) .

Si vous n’utilisez pas de package d’Windows Installer pour installer votre IME ou votre service de texte, il est fortement recommandé d’utiliser une application d’installation 64 bits. Le redirecteur du système de fichiers WOW64 peut entraîner la mise en place de fichiers dans les répertoires incorrects dans les programmes d’installation 32 bits (par exemple, la redirection du système de fichiers WOW64 peut entraîner l’installation des fichiers destinés au répertoire system32 dans le répertoire SysWOW64 à la place). Si vous devez utiliser un programme d’installation 32 bits, désactivez la redirection de fichiers WOW64 au cours du processus d’installation pour vous assurer que le service redirecteur de fichiers n’entraîne pas de redirection inattendue pendant le processus d’installation. Pour plus d’informations sur le redirecteur de système de fichiers WOW64, consultez [redirecteur de système de fichiers](/windows/desktop/WinProg64/file-system-redirector). Pour plus d’informations sur la façon de désactiver ou d’activer la redirection du système de fichiers WOW64, consultez [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection).

> [!TIP]
>
> Évitez les chemins d’installation codés en dur. Pour plus d’informations, consultez [localiser des répertoires à l’aide de l’interface de programmation d’applications non Hard-Coded chemins d’accès](/previous-versions//ms675638(v=vs.85))

 

> [!IMPORTANT]
>
> N’installez aucun fichier IME ou de service de texte dans le répertoire spécial% WINDIR% \\ IME (par défaut, c : \\ Windows \\ IME). Ce répertoire contient des fichiers système qui prennent en charge les services de texte et les éditeurs IME. elle n’est pas destinée à contenir des fichiers IME ou de service de texte tiers, et la redirection du système de fichiers WOW64 n’est pas prise en charge pour ce répertoire.

 

## <a name="dual-ctfmonexe-processes-run-on-64-bit-windows-platforms"></a>Les processus à double Ctfmon.exe s’exécutent sur des plateformes Windows 64 bits

Le processus de ctfmon.exe gère l’infrastructure de services de texte sur le bureau et fournit également l’interface utilisateur de la barre de langue. Sur Windows 64 bits, une version 32 bits et une version 64 bits du processus de ctfmon.exe s’exécutent simultanément. Le processus de ctfmon.exe 64 bits gère les services de texte 64 bits et, de même, le processus de ctfmon.exe de 32 bits gère les services de texte 32 bits.

## <a name="display-behavior-for-different-versions-of-the-language-bar-ui"></a>Comportement d’affichage pour les différentes versions de l’interface utilisateur de la barre de langue

Sur Windows 64 bits, seule l’interface utilisateur de la barre de langue associée à la version 64 bits d’un service de texte est toujours affichée. Dans les cas où une application 32 bits utilise la version 32 bits d’un service de texte, Windows 64 bits insère automatiquement l’interface utilisateur de la barre de langue pour le service de texte 64 équivalent. Cela garantit qu’aucun travail spécial n’est requis pour que les services de texte 32 bits s’affichent dans la version 64 bits de la barre de langue.

## <a name="control-panel-considerations-on-64-bit-windows"></a>Considérations sur le panneau de configuration sur Windows 64 bits

Windows 64 bits fournit un accès aux versions 32 bits et 64 bits des services de texte et des éditeurs IME via le panneau de configuration. Pour accéder aux paramètres du panneau de configuration pour des versions spécifiques de Text services ou des éditeurs IME, consultez les emplacements suivants.

-   **Accès au panneau de configuration pour les services de texte et les ime 32 bits :** Paramètres start->-> panneau de configuration-> afficher les icônes du panneau de configuration x86
-   **Accès au panneau de configuration pour les services de texte et les ime 64 bits :** Paramètres start->-> panneau de configuration-> Options régionales et linguistiques

Dans certains cas, certains paramètres peuvent être disponibles uniquement via le panneau de configuration 32 bits. Dans ce cas, assurez-vous que les utilisateurs de votre service de texte ou de l’éditeur IME en sont conscients, en fournissant la documentation appropriée ou en proposant des indicateurs d’interface utilisateur dans votre interface de paramètres 64 bits.

 

 