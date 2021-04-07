---
title: Contrôles Windows
description: Un contrôle est une fenêtre enfant qu’une application utilise conjointement à une autre fenêtre pour permettre l’interaction de l’utilisateur.
ms.assetid: 0a6eb481-d94e-40c5-afec-46354520f08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bf14f3c93f6f38ba787cba463977a4dca9eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028815"
---
# <a name="windows-controls"></a>Contrôles Windows

## <a name="purpose"></a>Objectif

Un contrôle est une fenêtre enfant qu’une application utilise conjointement à une autre fenêtre pour permettre l’interaction de l’utilisateur. Les contrôles sont souvent utilisés dans les boîtes de dialogue, mais ils peuvent également être utilisés dans d’autres fenêtres. Les contrôles dans les boîtes de dialogue offrent à l’utilisateur un moyen de taper du texte, de choisir des options et d’initier des actions. Les contrôles dans d’autres fenêtres fournissent un large éventail de services, tels que la possibilité pour l’utilisateur de choisir des commandes, d’afficher l’État et d’afficher et de modifier du texte. Cette documentation décrit les contrôles fournis par Windows et les éléments de programmation utilisés pour les créer et les manipuler.

Pour obtenir la liste de tous les contrôles Windows, y compris un lien vers une vue d’ensemble complète et des informations de référence pour chaque contrôle, consultez [bibliothèque de contrôles](individual-control-info.md).

## <a name="developer-audience"></a>Développeurs concernés

Les contrôles sont conçus pour être utilisés par les développeurs C/C++ et les concepteurs d’interface utilisateur. En général, les développeurs ont besoin d’un niveau modéré de compréhension des concepts de programmation d’interface utilisateur, de la programmation d’API Windows et d’Unicode.

## <a name="run-time-requirements"></a>Conditions d’exécution

La prise en charge des contrôles est assurée par User32.dll et Comctl32.dll. Pour plus d’informations, consultez [versions de contrôle courantes](common-control-versions.md).

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                             | Description                                                                                                                                     |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos des contrôles communs](common-controls-intro.md)<br/>                     | Fournit des informations générales qui sont communes à tous les contrôles pris en charge par Comctl32.dll.<br/>                                      |
| [Messages de contrôle](control-messages.md)<br/>                               | Explique comment les messages Windows sont utilisés pour communiquer avec les contrôles.<br/>                                                                 |
| [Contrôles personnalisés](user-controls-intro.md)<br/>                             | Décrit les différentes façons de créer des contrôles personnalisés. <br/>                                                                                 |
| [Contrôles de sous-classe](subclassing-overview.md)<br/>                       | Décrit un moyen de personnaliser un contrôle en modifiant ses fonctionnalités ou en en ajoutant de nouveaux. <br/>                                                 |
| [Dessin personnalisé](custom-draw.md)<br/>                                         | Décrit un service, fourni par certains contrôles, que les applications peuvent utiliser pour personnaliser divers aspects de l’apparence du contrôle. <br/> |
| [Considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md)<br/> | Fournit des informations sur les considérations de sécurité liées aux contrôles Windows. <br/>                                                 |
| [Bibliothèque de contrôles](individual-control-info.md)<br/>                         | Fournit des vues d’ensemble et des informations de référence sur chaque contrôle pris en charge par User32.dll et Comctl32.dll.<br/>                            |
| [Référence de contrôle générale](common-control-reference.md)<br/>              | Fournit des informations de référence sur les éléments de programmation qui s’appliquent à plusieurs contrôles, et pas uniquement à un contrôle spécifique.<br/>           |
| [Contrôler Spy v 2.0](control-spy.md)<br/>                                    | Décrit le contrôle Spy, un outil qui aide les développeurs à comprendre les contrôles communs. <br/>                                                     |
| [Styles visuels](themes-overview.md)<br/>                                   | Décrit comment l’apparence des contrôles peut varier selon le style visuel choisi par l’utilisateur. <br/>                               |
| [Format du fichier de thème](themesfileformat-overview.md)<br/>                     | Décrit le format des fichiers de thème (. Theme) utilisés dans Windows 7 et Windows Vista.<br/>                                                    |



 

 

 





