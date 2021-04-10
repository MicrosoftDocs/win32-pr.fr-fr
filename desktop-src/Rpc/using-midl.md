---
title: Utilisation de MIDL
description: Création et compilation d’une interface Microsoft Interface Definition Language (MIDL) et d’un appel de procédure distante (RPC).
ms.assetid: 2594e3d6-d44a-4e12-8286-b9700e67702e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22da60f20cba6c558c7f1a67478adef7b407d591
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730013"
---
# <a name="using-midl"></a>Utilisation de MIDL

Toutes les interfaces des programmes utilisant RPC doivent être définies en Microsoft Interface Definition Language (MIDL) et compilées avec le compilateur MIDL. Les rubriques suivantes présentent une brève présentation de la création et de la compilation d’une interface MIDL :

-   [Définition d’une interface avec MIDL](#defining-an-interface-with-midl)
-   [Compilation d’un fichier MIDL](#compiling-a-midl-file)

Pour une présentation détaillée de ces rubriques, consultez [les fichiers IDL et ACF](the-idl-and-acf-files.md).

## <a name="defining-an-interface-with-midl"></a>Définition d’une interface avec MIDL

Les fichiers MIDL sont des fichiers texte que vous pouvez créer et modifier à l’aide d’un éditeur de texte. Si vous générez un UUID pour votre interface, vous stockez généralement la sortie dans un fichier MIDL de modèle. Pour plus d’informations sur les UUID, consultez [génération d’UUID d’interface](generating-interface-uuids.md).

Toutes les interfaces dans MIDL suivent le même format. Ils commencent par un en-tête qui contient une liste d’attributs d’interface et le nom de l’interface. Les attributs sont placés entre crochets. L’en-tête d’interface est suivi de son corps, qui est placé entre accolades. Une interface simple est présentée dans l’exemple suivant :

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface MyInterface
{
  const unsigned short INT_ARRAY_LEN = 100;

  void MyRemoteProc( 
      [in] int param1,
      [out] int outArray[INT_ARRAY_LEN]
  );
}
```

Certains des attributs qui apparaissent généralement dans une définition d’interface MIDL sont l’UUID et le numéro de version de l’interface. Le corps de la définition d’interface doit contenir les déclarations de procédure de toutes les procédures distantes dans l’interface. Il peut également contenir les déclarations des types de données et des constantes requis par l’interface.

Tous les paramètres dans les déclarations de procédure distante doivent être déclarés comme \[ [**in**](/windows/desktop/Midl/in) \] , \[ [**out**](/windows/desktop/Midl/out-idl) \] ou \[ **in**, **out** \] . Ces déclarations spécifient que le programme client transmet les données dans une procédure distante, récupère les données d’une procédure distante, ou les deux. Pour plus d’informations sur les déclarations de paramètres d’interface, consultez [le corps de l’interface IDL](the-idl-interface-body.md).

## <a name="compiling-a-midl-file"></a>Compilation d’un fichier MIDL

Le compilateur MIDL est un outil en ligne de commande qui est automatiquement installé avec le kit de développement logiciel (SDK) de la plateforme. Appelez-le dans une fenêtre de commande en tapant la commande **MIDL**, suivie du nom d’un fichier MIDL, sur la ligne de commande. Assurez-vous que le répertoire contenant le compilateur MIDL se trouve dans votre chemin d’accès. L’exemple suivant illustre son utilisation :

**MyApp. idl MIDL**

Notez que vous n’avez pas besoin d’inclure l’extension si le nom de fichier a l’extension. idl. Vous pouvez également utiliser les [commutateurs de ligne de commande](/windows/desktop/Midl/midl-command-line-reference) du compilateur MIDL en les insérant entre la commande **MIDL** et le nom de fichier. Cela est illustré dans l’exemple suivant :

**MIDL/ACF MyApp. ACF MyApp. idl**

Dans cet exemple, le compilateur MIDL est exécuté à l’aide du fichier MyApp. idl comme fichier d’entrée. Le commutateur de ligne de commande **/ACF** indique au compilateur d’utiliser également un fichier de configuration d’application (ACF) pour l’entrée. Les fichiers de configuration de l’application sont décrits plus en détail dans [les fichiers IDL et ACF](the-idl-and-acf-files.md).

Pour plus d’informations sur l’utilisation du compilateur MIDL, consultez le [Microsoft Interface Definition Language (MIDL)](/windows/desktop/Midl/midl-start-page), qui contient des informations sur les rubriques suivantes :

-   [C-Configuration requise pour le préprocesseur pour MIDL](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [C/C++-considérations relatives au compilateur](/windows/desktop/Midl/c-c-compiler-considerations)
-   [Fichiers générés pour une interface RPC](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [Informations de référence sur la ligne de commande MIDL](/windows/desktop/Midl/midl-command-line-reference)
-   [Référence du langage MIDL](/windows/desktop/Midl/midl-language-reference)
-   [Erreurs et avertissements du compilateur MIDL](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 