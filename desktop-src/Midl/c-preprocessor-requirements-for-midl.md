---
title: C-Configuration requise pour le préprocesseur pour MIDL
description: Cette page s’applique uniquement aux développeurs qui ont des raisons spécifiques de remplacer le préprocesseur Microsoft C/C++ comme préprocesseur utilisé par MIDL, ou aux développeurs qui doivent spécifier des commutateurs de préprocesseur personnalisés.
ms.assetid: 1dd5eef4-5ea4-4958-8f53-9a95c0ccbf3e
keywords:
- MIDL du compilateur MIDL, C-preprocesseur, configuration requise
- C-preprocesseur MIDL, configuration requise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49c4e0c086a52eda2705d72cf2a2ff22c759290
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940191"
---
# <a name="c-preprocessor-requirements-for-midl"></a>C-Configuration requise pour le préprocesseur pour MIDL

Cette page s’applique uniquement aux développeurs qui ont des raisons spécifiques de remplacer le préprocesseur Microsoft C/C++ comme préprocesseur utilisé par MIDL, ou aux développeurs qui doivent spécifier des commutateurs de préprocesseur personnalisés. Les commutateurs MIDL [**/CPP \_ cmd**](-cpp-cmd.md), [**/CPP \_ OPT**](-cpp-opt.md)et [**/non \_ CPP**](-no-cpp-nocpp.md) sont utilisés pour remplacer le comportement par défaut du compilateur. Il n’y a généralement aucune raison de remplacer le préprocesseur Microsoft C/C++, ni de spécifier des commutateurs de préprocesseur personnalisés.

Le compilateur MIDL utilise un préprocesseur C lors du traitement initial du fichier IDL. L’environnement de génération utilisé lors de la compilation des fichiers IDL est associé à un préprocesseur C/C++ par défaut. Si un autre préprocesseur doit être utilisé, le commutateur de compilateur MIDL [**/CPP \_ cmd**](-cpp-cmd.md) active une substitution du nom de préprocesseur C/C++ par défaut :

``` syntax
midl /cpp_cmd preprocessor_name filename
```

<dl> <dt>

<span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*nom du préprocesseur \_*
</dt> <dd>

Spécifie le nom du préprocesseur à utiliser par MIDL. Peut être spécifié avec un chemin d’accès au fichier binaire. L’extension. exe est facultative.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extension*
</dt> <dd>

Spécifie le nom du fichier IDL.

</dd> </dl>

-   Le compilateur MIDL s’attend à ce que le préprocesseur respecte les conventions suivantes :
-   Le fichier d’entrée est spécifié en tant que dernier argument sur la ligne de commande.
-   Le préprocesseur doit rediriger la sortie vers le périphérique de sortie standard, stdout.
-   Dans le flux de sortie du préprocesseur, les directives de **\# ligne** sont présentes pour permettre de meilleurs messages de diagnostic.
-   Les directives de ligne sont les seules directives de préprocesseur dans le flux de sortie.

MIDL part du principe que le préprocesseur généré a supprimé toutes les directives de préprocesseur du flux d’entrée du compilateur, à l’exception des occurrences de la directive de ligne nécessaire pour identifier l’emplacement source dans les messages du compilateur. Lorsque vous indiquez un préprocesseur différent du préprocesseur Microsoft C/C++, ou lorsque vous spécifiez des options de préprocesseur avec le commutateur [**/CPP \_ OPT**](-cpp-opt.md) , la spécification d’une option de préprocesseur appropriée qui place les directives de ligne dans le flux d’entrée du compilateur est requise. Par exemple, pour le préprocesseur Microsoft C/C++, l’option **/e** devrait être utilisée :

``` syntax
midl /cpp_cmd cl.exe /cpp_opt "/E" file.idl
```

La directive de **\# ligne** est acceptée par MIDL sous l’une des formes suivantes :

``` syntax
#line digit-sequence "filename" new-line
 
# digit-sequence "filename" new-line
```

Pour obtenir une description complète de la directive de ligne et des autres directives de préprocesseur, consultez la documentation du compilateur C utilisé.

MIDL accepte uniquement la directive de préprocesseur de ligne. Par conséquent, si le commutateur [**/non \_ CPP**](-no-cpp-nocpp.md) est utilisé, le fichier d’entrée ne doit pas avoir d’autres directives de préprocesseur ou le fichier d’entrée doit avoir été traité avant l’appel de MIDL.

Pour plus d’informations, consultez [gestion des \# définitions dans les fichiers IDL](dealing-with-defines-in-idl-files-2.md).

 

 




