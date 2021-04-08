---
description: ICE82 vérifie que l’action RegisterProduct, l’action RegisterUser, l’action PublishProduct et l’action PublishFeatures sont toutes présentes dans la table InstallExecuteSequence. Le package est validé si toutes les actions sont présentes.
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa6ba2e0bd07af06bf90c604c333966b5581ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758415"
---
# <a name="ice82"></a>ICE82

ICE82 vérifie que l’action [RegisterProduct](registerproduct-action.md), l' [action RegisterUser](registeruser-action.md), l’action [PublishProduct](publishproduct-action.md)et l' [action PublishFeatures](publishfeatures-action.md) sont toutes présentes dans la [table InstallExecuteSequence](installexecutesequence-table.md). Le package est validé si toutes les actions sont présentes.

ICE82 publie un avertissement s’il y a deux actions avec le même numéro de séquence répertorié dans les tables InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence ou AdvtExecuteSequence.

## <a name="result"></a>Résultats

ICE82 publie les avertissements suivants.



| AVERTISSEMENT ICE82                                                                                                                                                                                                                 | Description                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La table InstallExecuteSequence ne contient pas l’ensemble des actions mentionnées ci-dessous : actions manquantes :<br/> Publier les fonctionnalités<br/> Publier le produit<br/> Inscrire le produit<br/> Inscrire un utilisateur<br/> | L’action personnalisée ICE82 publie un avertissement si les quatre actions sont absentes.                                                                                                                                         |
| \[ \] Le numéro de séquence 2 de l’action 1 est dupliqué \[ \] dans le tableau \[ 3 \] .                                                                                                                                                     | ICE82 publie un avertissement s’il y a deux actions avec le même numéro de séquence répertorié dans les tables InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence ou AdvtExecuteSequence. |



 

ICE82 publie les erreurs suivantes.



| Erreur ICE82                                                                                                                                                                                                                                        | Description                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| Le InstallExecuteSequence doit contenir toutes les actions mentionnées ci-dessous ou aucune des actions présentes<br/> <List of actions present> <br/> Actions manquantes :<br/> <List of actions missing> <br/> | ICE82 publie une erreur si certaines des quatre actions sont présentes et que d’autres sont absentes. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 




