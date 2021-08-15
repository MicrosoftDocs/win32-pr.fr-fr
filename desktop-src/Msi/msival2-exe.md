---
description: Msival2.exe est un utilitaire de ligne de commande qui peut exécuter une suite d’évaluateurs de cohérence internes (ICEs).
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8ed1228413d5b2fab0dfab79ea4546a9d15e74c8c62e9b1ca9751699f469854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943876"
---
# <a name="msival2exe"></a>Msival2.exe

Msival2.exe est un utilitaire de ligne de commande qui peut exécuter une suite d' [évaluateurs de cohérence internes (ICEs)](internal-consistency-evaluators-ices.md).

cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

Pour plus d’informations sur le fichier ICEs et le fichier CUB, consultez [utilisation des évaluateurs de cohérence internes](using-internal-consistency-evaluators.md).

## <a name="syntax"></a>Syntaxe

**MSIVal2** *{Database} {fichier CUB} \[ -f \] \[ -l {logfile} \] \[ -i {Ice ID} \[ : {Ice ID}... \] \]*

## <a name="command-line-options"></a>Options de la ligne de commande

Msival2.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse. Un séparateur de barre oblique peut également être utilisé à la place d’un tiret.



| Option | Description                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -f     | Filtrez tous les messages d’information à partir des résultats affichés. Tous les autres types de messages s’affichent.                                                                                                                                                                                              |
| -i     | Exécutez uniquement le CIEM indiqué sur la ligne de commande dans l’ordre spécifié. Chaque action personnalisée ICE doit être indiquée telle qu’elle apparaît dans la [table CustomAction](customaction-table.md) du fichier CUB. Si cette option est omise, l’outil exécute l’ensemble par défaut du CIEM spécifié par l’auteur du fichier CUB. |
| -l     | Écrit les résultats dans le fichier spécifié. Le fichier ne doit pas déjà exister. Si le fichier existe, il n’est pas remplacé.                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Outils de développement du programme d’installation](windows-installer-development-tools.md)
</dt> <dt>

[Évaluateurs de cohérence internes-CIEM](internal-consistency-evaluators-ices.md)
</dt> <dt>

[Versions, outils et redistribuables publiés](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



