---
title: Appel du compilateur MIDL
description: Le compilateur MIDL peut générer du code pour différentes plateformes et versions système. Consultez le commutateur/target pour en savoir plus sur les commutateurs suggérés et sur la façon de générer du code optimisé pour une version particulière.
ms.assetid: 57730efa-71c3-4746-83f4-c7e327888efc
keywords:
- Compilateur MIDL MIDL, appeler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7e03abc49007b823f509acb35bd34ce6e47d80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/15/2019
ms.locfileid: "106510848"
---
# <a name="invoking-the-midl-compiler"></a>Appel du compilateur MIDL

Le compilateur MIDL peut générer du code pour différentes plateformes et versions système. Consultez le commutateur [**/target**](-target.md) pour en savoir plus sur les commutateurs suggérés et sur la façon de générer du code optimisé pour une version particulière.

Exécutez le compilateur MIDL à partir de la ligne de commande à l’aide de la commande suivante :

 *<  options >* MIDL **NomFichier. idl**

où *<  options >* représente les options de ligne de commande que vous souhaitez utiliser, et nom_fichier. idl est le nom du fichier MIDL à compiler.

Une liste complète des commutateurs et options du compilateur MIDL est disponible quand vous utilisez le compilateur MIDL [**/Help**](-help-.md) et/ ? Active. Les commutateurs sont organisés par catégories. Pour plus d’informations, consultez la [Référence du Command-Line MIDL](midl-command-line-reference.md).

> [!NOTE]
> Le nouvel indicateur global **$ ( \_ optimisation MIDL)** existe dans Win32. mak. Lorsqu’un fichier. idl est compilé à l’aide de cet indicateur, le stub généré peut utiliser les fonctionnalités RPC les plus récentes disponibles sur la plateforme spécifiée et améliorer potentiellement les performances et la stabilité de l’application. Il est recommandé que les applications utilisent cet indicateur lors de l’utilisation de MIDL.
>
> **MIDL** **$ ( \_ optimisation MIDL)** **...**