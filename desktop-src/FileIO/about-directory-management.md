---
description: Un répertoire qui contient un ou plusieurs répertoires est le parent du répertoire ou des répertoires contenus, et chaque répertoire contenu est un enfant du répertoire parent. La structure hiérarchique des répertoires est appelée arborescence de répertoires.
ms.assetid: e8a7bf82-0f3c-4ad9-9d10-25c4d69733dc
title: À propos de la gestion d’annuaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9cc59e465e1d97b28b1cfdff35c5f288e56b5eb0ee9800273873ffe6476868b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766409"
---
# <a name="about-directory-management"></a>À propos de la gestion d’annuaire

Un répertoire qui contient un ou plusieurs répertoires est le *parent* du répertoire ou des répertoires contenus, et chaque répertoire contenu est un *enfant* du répertoire parent. La structure hiérarchique des répertoires est appelée *arborescence de répertoires*.

Le système de fichiers NTFS implémente le lien logique entre un répertoire et les fichiers qu’il contient comme *table d’entrée de répertoire*. Lorsqu’un fichier est déplacé dans un répertoire, une entrée est créée dans la table pour le fichier déplacé et le nom du fichier est placé dans l’entrée. Lorsqu’un fichier contenu dans un répertoire est supprimé, le nom et l’entrée correspondant au fichier supprimé sont également supprimés de la table. Il peut exister plusieurs entrées pour un seul fichier dans une table d’entrée de répertoire. Si une entrée supplémentaire est créée dans la table pour un fichier, cette entrée est appelée un *lien physique* vers ce fichier. Il n’existe aucune limite au nombre de liens physiques qui peuvent être créés pour un seul fichier.

Les répertoires peuvent également contenir des jonctions et des points d’analyse.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                 | Description                                                                                            |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Création et suppression de répertoires](creating-and-deleting-directories.md)<br/> | Une application peut créer et supprimer par programmation des répertoires.<br/>                          |
| [Handles de répertoire](obtaining-a-handle-to-a-directory.md)<br/>                 | Chaque fois qu’un processus crée ou ouvre un objet d’annuaire, il reçoit un descripteur de l’objet.<br/> |
| [Points d'analyse](reparse-points.md)<br/>                                       | Décrit les points d’analyse.<br/>                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur la gestion d’annuaire](directory-management-reference.md)
</dt> </dl>

 

 




