---
title: Importation de fichiers et de bibliothèques de types
description: Les mots clés MIDL incluent, import et importlib vous permettent de réutiliser du code en référençant des fichiers d’en-tête, IDL et ODL (Object Definition Language) existants, ainsi que des bibliothèques de types compilés.
ms.assetid: b4571c1d-4bd7-4ab1-9ef6-14356a6c4bb4
keywords:
- Microsoft Interface Definition Language MIDL, tâches, importation de fichiers et de bibliothèques de types
- importation de MIDL
- bibliothèques de types MIDL, importation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b740f29726c1ce4d401fc69b2ea07e811eac0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104322573"
---
# <a name="importing-files-and-type-libraries"></a>Importation de fichiers et de bibliothèques de types

Les mots clés MIDL [**incluent**](include.md), [**Import**](import.md)et [**importlib**](importlib.md) vous permettent de réutiliser du code en référençant des fichiers d’en-tête, IDL et ODL (Object Definition Language) existants, ainsi que des bibliothèques de types compilés.

La directive CCP [**include**](include.md) vous permet de spécifier dans un fichier ACF un ou plusieurs fichiers d’en-tête C à inclure dans le code stub généré par MIDL. Le fichier généré aura une ligne avec une directive de préprocesseur C **\# include** avec le fichier d’en-tête indiqué. Utilisez cette directive **include** pour importer des fichiers d’en-tête spécifiques à un environnement d’exploitation particulier et qui ne contiennent pas les informations nécessaires à l’interface entre le client et le serveur. N’utilisez pas **include** pour les fichiers d’en-tête contenant des types de données que vous souhaitez accéder au fichier IDL. Utilisez plutôt la directive [**Import**](import.md) .

## <a name="example-1"></a>Exemple 1

``` syntax
[
  auto_handle
] 
interface X86PC
{ 
  include "gendefs.h", "protos.h", "myfile.h"; 
  //interface typdefs and function declarations here
}
```

La directive d' [**importation**](import.md) IDL est la méthode standard pour placer les définitions de type et d’interface à partir d’autres fichiers IDL (ou ODL) et de fichiers d’en-tête dans votre fichier IDL. Toutes les instructions IDL dans le fichier importé, telles que typedefs, les déclarations [**const**](const.md) et les définitions d’interface, deviennent disponibles dans le fichier IDL d’importation.

À l’instar de la directive de préprocesseur du langage C **\# include**, la directive [**Import**](import.md) indique au compilateur d’inclure les types de données définis dans les fichiers IDL importés. Contrairement à la directive **\# include** , la directive **Import** ignore les prototypes de procédure, car aucun stub n’est généré pour quoi que ce soit dans le fichier importé. Étant donné que le préprocesseur est appelé séparément pour le fichier importé, les directives de préprocesseur (telles que * *) ne sont pas reportées dans le fichier IDL d’importation.

Pour plus d’informations sur l’utilisation de l' [**importation**](import.md) pour inclure des fichiers d’en-tête système dans un fichier IDL, consultez [importation de fichiers d’en-tête système](importing-system-header-files.md).

## <a name="example-2"></a>Exemple 2

``` syntax
[
  uuid(. . .), object
] 
interface IKnown : IUnknown
{
  import "base.idl", "unknwn.idl", "helper.idl";
  //remainder of interface definition
}
```

La directive ODL [**importlib**](importlib.md) vous permet de référencer une bibliothèque de types compilée dans votre fichier IDL ou ODL. La directive **importlib** doit se trouver à l’intérieur d’une instruction [**Library**](library.md) et doit précéder d’autres descriptions de type dans la bibliothèque. La bibliothèque importée, ainsi que la bibliothèque générée, doivent être accessibles à l’application au moment de l’exécution.

## <a name="example-3"></a>Exemple 3

``` syntax
library NewBrowser
{
  importlib("stdole32.tlb");
  importlib("legacy.tlb");
  //remainder of library definition
};
```

Vous pouvez également utiliser la directive C-preprocesseur **\# include** pour inclure des en-têtes et d’autres fichiers dans votre fichier IDL ou ODL. N’oubliez pas, toutefois, que cette directive inclura littéralement le contenu entier du fichier spécifié. Si un fichier d’en-tête contient des prototypes dont vous n’avez pas besoin ou que vous ne souhaitez pas dans les fichiers stub générés par MIDL, ou s’il contient des définitions de type non accessibles à distance, vous devez utiliser la directive d' [**importation**](import.md) MIDL au lieu de la directive **\# include** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**port**](import.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**inclusion**](include.md)
</dt> <dt>

[Importation de fichiers d’en-tête système](importing-system-header-files.md)
</dt> </dl>

 

 




