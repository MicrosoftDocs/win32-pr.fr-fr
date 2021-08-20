---
title: MkTypLib Command-Line outil
description: MkTypLib est une application de ligne de commande qui traite un fichier IDL pour produire une bibliothèque de types. Il peut également être utilisé pour générer un fichier d’en-tête C ou C++.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b712ed8220dd609dd3ba189bdac6b5ee11d2805f26ff5a1f146c20f17c1f8ab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047937"
---
# <a name="mktyplib-command-line-tool"></a>MkTypLib Command-Line outil

\[L’outil Mktyplib.exe est obsolète. Utilisez plutôt le compilateur MIDL. Si vous avez besoin d’une compatibilité descendante avec les anciens programmes d’automatisation, utilisez le compilateur MIDL avec l’option **/mktyplib203** .\]

MkTypLib est une application de ligne de commande qui traite un fichier IDL pour produire une bibliothèque de types. Il peut également être utilisé pour générer un fichier d’en-tête C ou C++.

Pour générer une bibliothèque de types à partir d’un fichier ODL :

-   Exécutez la commande suivante à partir de l'invite de commande :

    * * mktyplibÂ * *_nom de fichier_

    où *filename* est le nom du fichier ODL.

MkTypLib prend également en charge plusieurs paramètres facultatifs. Pour obtenir la liste complète, exécutez la ligne de commande suivante :

**mktyplib/ ?**

Comme MkTypLib est une application obsolète, il ne peut pas analyser des fichiers IDL ou des fichiers avec des interfaces définies en dehors d’une instruction de [**bibliothèque**](/windows/desktop/Midl/library) . Pour plus d’informations, consultez [différences entre MIDL et mktyplib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Traduire en C++](translating-to-c--.md)
</dt> </dl>

 

 