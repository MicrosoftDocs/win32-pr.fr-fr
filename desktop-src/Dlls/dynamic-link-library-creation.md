---
description: Pour créer une bibliothèque de Dynamic-Link (DLL), vous devez créer un ou plusieurs fichiers de code source, et éventuellement un fichier de l’éditeur de liens pour exporter les fonctions.
ms.assetid: b66ea0e8-84c3-40be-bf02-765b9dd61f9f
title: Création de la bibliothèque de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12d296b1494cfcedcdfa823eb1a3dd4d408427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753780"
---
# <a name="dynamic-link-library-creation"></a>Création de la bibliothèque de Dynamic-Link

Pour créer une bibliothèque de Dynamic-Link (DLL), vous devez créer un ou plusieurs fichiers de code source, et éventuellement un fichier de l’éditeur de liens pour exporter les fonctions. Si vous prévoyez d’autoriser les applications qui utilisent votre DLL à utiliser la liaison dynamique au moment du chargement, vous devez également créer une bibliothèque d’importation.

## <a name="creating-source-files"></a>Création de fichiers sources

Les fichiers sources d’une DLL contiennent des fonctions et des données exportées, des fonctions et des données internes, ainsi qu’une [fonction de point d’entrée](dynamic-link-library-entry-point-function.md) facultative pour la dll. Vous pouvez utiliser tous les outils de développement qui prennent en charge la création de dll Windows.

Si votre DLL peut être utilisée par une application multithread, vous devez rendre votre DLL « thread-safe ». Vous devez synchroniser l’accès à toutes les données globales de la DLL pour éviter l’endommagement des données. Vous devez également vous assurer que vous effectuez un lien uniquement avec des bibliothèques thread-safe. Par exemple, Microsoft Visual C++ contient plusieurs versions de la bibliothèque Runtime C, une qui n’est pas thread-safe et deux qui sont.

## <a name="exporting-functions"></a>Exportation de fonctions

La façon dont vous spécifiez les fonctions d’une DLL à exporter dépend des outils que vous utilisez pour le développement. Certains compilateurs vous permettent d’exporter une fonction directement dans le code source en utilisant un modificateur dans la déclaration de la fonction. Dans d’autres cas, vous devez spécifier des exportations dans un fichier que vous transmettez à l’éditeur de liens.

Par exemple, à l’aide de Visual C++, il existe deux façons d’exporter des fonctions dll : avec le modificateur [**\_ \_ declspec (dllexport)**](https://msdn.microsoft.com/library/3y1sfaz2(v=VS.71).aspx) ou avec un fichier de définition de module (. def). Si vous utilisez le modificateur **\_ \_ declspec (dllexport)** , il n’est pas nécessaire d’utiliser un fichier. def. Pour plus d’informations, consultez [exportation à partir d’une dll](/cpp/build/exporting-from-a-dll?view=vs-2019).

## <a name="creating-an-import-library"></a>Création d’une bibliothèque d’importation

Un fichier de bibliothèque d’importation (. lib) contient des informations dont l’éditeur de liens a besoin pour résoudre les références externes aux fonctions DLL exportées, de sorte que le système puisse localiser la DLL spécifiée et les fonctions DLL exportées au moment de l’exécution. Vous pouvez créer une bibliothèque d’importation pour votre DLL lorsque vous générez votre DLL.

Pour plus d’informations, consultez [génération d’une bibliothèque d’importation et d’un fichier d’exportation](/cpp/build/reference/building-an-import-library-and-export-file?view=vs-2019).

## <a name="using-an-import-library"></a>Utilisation d’une bibliothèque d’importation

Par exemple, pour appeler la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) , vous devez lier votre code à la bibliothèque d’importation user32. lib. La raison en est que **CreateWindow** réside dans une DLL système nommée User32.dll et user32. lib est la bibliothèque d’importation utilisée pour résoudre les appels aux fonctions exportées dans User32.dll dans votre code. L’éditeur de liens crée une table qui contient l’adresse de chaque appel de fonction. Les appels aux fonctions dans une DLL sont résolus lors du chargement de la DLL. Pendant l’initialisation du processus, le système charge User32.dll, car le processus dépend des fonctions exportées dans cette DLL et met à jour les entrées dans la table des adresses de la fonction. Tous les appels à **CreateWindow** appellent la fonction exportée à partir de User32.dll.

Pour plus d’informations, consultez [liaison implicite avec une dll](/previous-versions/d14wsce5(v=vs.140)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une bibliothèque de liens dynamiques simple](creating-a-simple-dynamic-link-library.md)
</dt> <dt>

[Dll (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
