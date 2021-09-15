---
description: Si une application isolée spécifie une dépendance d’assembly, côte à côte recherche d’abord l’assembly parmi les assemblys partagés dans le dossier WinSxS.
ms.assetid: 93496631-55cc-4dd9-9a51-b748c35fd477
title: Séquence de recherche d’assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc689ecb14c55f0e8a609c7e7497fce969e88b8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238122"
---
# <a name="assembly-searching-sequence"></a>Séquence de recherche d’assemblys

Si une application isolée spécifie une dépendance d’assembly, côte à côte recherche d’abord l’assembly parmi les [assemblys partagés](/windows/desktop/Msi/shared-assemblies) dans le dossier WinSxS. Si l’assembly requis est introuvable, côte à côte, recherche un assembly privé installé dans un dossier de la structure de répertoires de l’application.

Les [assemblys privés](/windows/desktop/Msi/private-assemblies) peuvent être déployés aux emplacements suivants dans la structure de répertoires de l’application :

-   Dans le dossier de l’application. En règle générale, il s’agit du dossier contenant le fichier exécutable de l’application.
-   Dans un sous-dossier du dossier de l’application. Le sous-dossier doit avoir le même nom que l’assembly.
-   Dans un sous-dossier spécifique à une langue dans le dossier de l’application. Le nom du sous-dossier est une chaîne de codes de langue DHTML indiquant une langue ou une culture de langue.
-   Dans un sous-dossier d’un sous-dossier spécifique à une langue dans le dossier de l’application. Le nom du sous-dossier supérieur est une chaîne de codes de langue DHTML indiquant une langue ou une culture de langue. Le sous-dossier plus profond porte le même nom que l’assembly.

La première fois, côte à côte recherche un assembly privé, il détermine si un sous-dossier spécifique à la langue existe dans la structure de répertoires de l’application. S’il n’existe pas de sous-dossier spécifique à une langue, côte à côte recherche l’assembly privé aux emplacements suivants à l’aide de la séquence suivante.

1.  Côte à côte recherche le dossier WinSxS.
2.  \\\\< > \\ appdir < *AssemblyName* # C0.DLL
3.  \\\\< > \\ appdir < *assemblyname*>. manifest
4.  \\\\< > \\ appdir <  > \\ AssemblyName < *AssemblyName* # C0.DLL
5.  \\\\< > \\ appdir <  > \\ AssemblyName < *assemblyname*>. manifest

Si un sous-dossier spécifique à une langue existe, la structure de répertoire de l’application peut contenir l’assembly privé localisé dans plusieurs langues. Côte à côte recherche les sous-dossiers spécifiques à une langue pour s’assurer que l’application utilise la langue spécifiée ou la meilleure langue disponible. Les sous-dossiers spécifiques à une langue sont nommés à l’aide d’une chaîne de codes de langue DHTML qui spécifient une langue ou une culture de langue. Si un sous-dossier spécifique à une langue existe, les recherches côte à côte de l’assembly privé se trouvent aux emplacements suivants à l’aide de la séquence suivante.

1.  Côte à côte recherche le dossier WinSxS.
2.  \\\\< > \\ appdir < *langue-culture* > \\ < *AssemblyName* # C0.DLL
3.  \\\\< > \\ appdir < *langue-culture* > \\ < *assemblyname*>. manifest
4.  \\\\< > \\ appdir < *langue-culture* > \\ <  > \\ AssemblyName < *AssemblyName* # C0.DLL
5.  \\\\< > \\ appdir < *langue-culture* > \\ <  > \\ AssemblyName < *assemblyname*>. manifest

Notez que la séquence de recherche côte à côte trouve un fichier DLL portant le nom de l’assembly et s’arrête avant de rechercher un fichier manifeste portant le nom de l’assembly. La méthode recommandée pour gérer un assembly privé qui est une DLL consiste à placer le manifeste de l’assembly dans le fichier DLL en tant que ressource. L’ID de ressource doit être égal à 1 et le nom de l’assembly privé peut être le même que le nom de la DLL. Par exemple, si le nom de la DLL est MICROSOFT.WINDOWS.MYSAMPLE.DLL, la valeur de l’attribut Name utilisé dans l’élément **assemblyIdentity** du manifeste de l’assembly peut également être Microsoft. Windows. mysample. En guise d’alternative, vous pouvez placer le manifeste de l’assembly dans un fichier distinct. Toutefois, le nom de l’assembly et son manifeste doivent être différents du nom de la DLL. Par exemple, Microsoft. Windows. mysampleAsm, Microsoft. Windows. mysampleAsm. manifest et MICROSOFT.WINDOWS.MYSAMPLE.DLL.

Par exemple, si MyApp est installé à la racine du lecteur c : et requiert MyAsm en français-belge, côte à côte utilise la séquence suivante pour rechercher la meilleure approximation pour une instance localisée de MyAsm.

1.  Les recherches côte à côte WinSxS pour la version fr-is.
2.  c : \\ MyApp \\ fr-être \\myasm.dll
3.  c : \\ MyApp \\ fr-to \\ MyAsm. manifest
4.  c : \\ MyApp \\ fr- \\ MyAsm \\myasm.dll
5.  c : \\ MyApp \\ fr-être \\ MyAsm \\ MyAsm. manifest
6.  Les recherches côte à côte WinSxS pour la version fr.
7.  c : \\ MyApp \\ fr \\myasm.dll
8.  c : \\ MyApp \\ fr \\ MyAsm. manifest
9.  c : \\ MyApp \\ fr \\ MyAsm \\myasm.dll
10. c : \\ MyApp \\ fr \\ MyAsm \\ MyAsm. manifest
11. Les recherches côte à côte WinSxS pour la version en-US.
12. c : \\ MonApp \\ en-US \\myasm.dll
13. c : \\ MonApp \\ en-US \\ MyAsm. manifest
14. c : \\ MyApp \\ en-us \\ MyAsm \\myasm.dll
15. c : \\ MyApp \\ en-US \\ MyAsm \\ MyAsm. manifest
16. Les recherches côte à côte WinSxS pour la version en.
17. c : \\ MyApp \\ en \\myasm.dll
18. c : \\ MyApp \\ en \\ MyAsm. manifest
19. c : \\ MyApp \\ en \\ MyAsm \\myasm.dll
20. c : \\ MyApp \\ en \\ MyAsm \\ MyAsm. manifest
21. Les recherches côte à côte WinSxS pour la version sans langue.
22. c : \\ myapp \\myasm.dll
23. c : \\ MyApp \\ MyAsm. manifest
24. c : \\ MyApp \\ MyAsm \\myasm.dll
25. c : \\ MyApp \\ MyAsm \\ MyAsm. manifest

si la recherche côte à côte atteint une version indépendante du langage de l’assembly et qu’une version [MUI (multilanguage User Interface)](/windows/desktop/Intl/multilingual-user-interface) de Windows est présente sur le système, côte à côte, tente alors de lier à <*assemblyname*>. MUI. Côte à côte n’essaie pas d’effectuer une liaison à <*assemblyname*>. mui si la recherche atteint une version localisée de l’assembly. Le [manifeste d’assembly](assembly-manifests.md) d’un assembly indépendant du langage n’aura pas d’attribut de langage dans son élément **assemblyIdentity** . Si côte à côte atteint un assembly indépendant de la langue et que l’interface MUI est installée, côte à côte recherche les emplacements suivants à l’aide de la séquence suivante pour <*assemblyname*>. mui. Side-by-Side utilise la même séquence de recherche si l’assembly est indépendant de la culture, sauf <aucune recherche de *langue*> n’est effectuée.

1.  Côte à côte recherche le dossier WinSxS pour <*assemblyname*>. mui.
2.  \\\\<*langue de l’utilisateur-culture* > \\ < *assemblyname*>. mui
3.  \\\\<langue de l' *utilisateur* > \\ < *assemblyname*>. mui
4.  \\\\<*langue du système-Culture* > \\ < *assemblyname*>. mui
5.  \\\\< > langue \\ du < système *assemblyname*>. mui
6.  \\\\<*pas de langue* > \\ < *assemblyname*>. mui

Par exemple, si la recherche côte à côte trouve l’assembly privé sur c : \\ MyApp \\ MyAsm \\ MyAsm. manifest, et MyAsm est un assembly indépendant du langage. Côte à côte, utilise la séquence suivante pour rechercher MyAsm. mui. Notez que côte à côte ne recherche pas un assembly MUI indépendant de la langue.

1.  Les recherches côte à côte WinSxS pour la version fr-is de l’assembly MUI.
2.  c : \\ MyApp \\ fr-être \\myasm.mui.dll
3.  c : \\ MyApp \\ fr-to \\ MyAsm. mui. manifest
4.  c : \\ MyApp \\ fr- \\ MyAsm \\myasm.mui.dll
5.  c : \\ MyApp \\ fr-to \\ MyAsm \\ MyAsm. mui. manifest
6.  Les recherches côte à côte WinSxS pour la version fr de l’assembly MUI.
7.  c : \\ MyApp \\ fr \\myasm.mui.dll
8.  c : \\ MyApp \\ fr \\ MyAsm. mui. manifest
9.  c : \\ MyApp \\ fr \\ MyAsm \\myasm.mui.dll
10. c : \\ MyApp \\ fr \\ MyAsm \\ MyAsm. mui. manifest
11. Les recherches côte à côte WinSxS pour la version en-US de l’assembly MUI.
12. c : \\ MonApp \\ en-US \\myasm.mui.dll
13. c : \\ MonApp \\ en-US \\ MyAsm. mui. manifest
14. c : \\ MyApp \\ en-us \\ MyAsm \\myasm.mui.dll
15. c : \\ MyApp \\ en-US \\ MyAsm \\ MyAsm. mui. manifest
16. Les recherches côte à côte WinSxS pour la version en de l’assembly MUI.
17. c : \\ MyApp \\ en \\myasm.mui.dll
18. c : \\ MyApp \\ en \\ MyAsm. mui. manifest
19. c : \\ MyApp \\ en \\ MyAsm \\myasm.mui.dll
20. c : \\ MyApp \\ en \\ MyAsm \\ MyAsm. mui. manifest

 

 
