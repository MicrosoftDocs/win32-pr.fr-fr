---
title: Erreurs et avertissements du compilateur MIDL
description: Lors de l’utilisation du compilateur MIDL, les erreurs et les avertissements peuvent être provoqués par une utilisation incorrecte des commutateurs de ligne de commande ou par le contenu des fichiers IDL et ACF.
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- Microsoft Interface Definition Language MIDL, référence
- MIDL du compilateur MIDL, Erreurs
- MIDL du compilateur, Erreurs
- Erreurs MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae531528f83f3731b4449c7aba012f3228edd9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839077"
---
# <a name="midl-compiler-errors-and-warnings"></a>Erreurs et avertissements du compilateur MIDL

Lors de l’utilisation du compilateur MIDL, les erreurs et les avertissements peuvent être provoqués par une utilisation incorrecte des commutateurs de ligne de commande ou par le contenu des fichiers IDL et ACF. Si l’erreur est due à l’entrée incorrecte des commutateurs de ligne de commande, un message d’erreur ou d’avertissement peut spécifier le nom d’un ou plusieurs commutateurs du compilateur MIDL. Par exemple, vous pouvez inclure certains attributs ACF dans un fichier IDL lorsque vous utilisez le commutateur/de **\_ configuration d’application** , mais ce fichier IDL génère une erreur si vous compilez sans utiliser le commutateur/**app \_ config** .

Les erreurs dans les fichiers IDL et ACF se répartissent en deux catégories : les erreurs interceptées par le préprocesseur et les erreurs reconnues par le compilateur. Cette section répertorie les messages d’erreur du compilateur et du préprocesseur MIDL. Il décrit également leurs formats et leurs causes.

-   [Formats des messages d’erreur et d’avertissement](error-and-warning-message-formats.md)
-   [Erreurs de préprocesseur](preprocessor-errors.md)
-   [Erreurs du compilateur](compiler-errors.md)

 

 




