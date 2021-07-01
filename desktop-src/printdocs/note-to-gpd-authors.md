---
description: Passez en revue les mots clés GPD sans équivalents de document PrintCapabilities. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: f1b94241-5376-423f-b10a-336dc47f3d59
title: Note aux auteurs GPD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52fe9d0c4ce36cf603d492688f4faa426e3050b9
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119814"
---
# <a name="note-to-gpd-authors"></a>Note aux auteurs GPD

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Pour les auteurs de documents PrintCapabilities connaissant les fichiers GPD, certains mots clés GPD n’ont pas d’équivalent dans le document PrintCapabilities. Le tableau suivant contient les mots clés GPD sans un document PrintCapabilities équivalent, et la raison pour laquelle il n’existe aucun équivalent.



| Mot clé GPD                                                                            | Explication                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*Contraintes<br/> \*InvalidCombination<br/> \*ConflictPriority<br/> | Les contraintes ne sont pas définies dans le document PrintCapabilities, car les clients PrintCapabilities ne sont pas censés les traiter, les appliquer ou les résoudre. Ces tâches sont laissées au fournisseur PrintTicket pour effectuer la validation PrintTicket. Les plug-ins Unidrv peuvent fournir leur propre code de validation PrintTicket, ou ils peuvent s’appuyer sur Unidrv pour effectuer cette validation. Dans ce dernier cas, Unidrv applique toutes les contraintes définies dans le fichier GPD.<br/> Les pilotes monolithiques doivent fournir leur propre code de validation PrintTicket et doivent fournir leur propre méthode d’expression et d’application de contraintes.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \*DefaultOption<br/>                                                             | Il existe une méthode PrintTicket qui retourne un PrintTicket par défaut, qui, par définition, possède tous les paramètres par défaut pour chaque fonctionnalité.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \*FeatureType<br/>                                                               | Une fonctionnalité peut être divisée en trois catégories différentes :<br/> Fonctionnalité dont les paramètres sont définis dans un PrintTicket. Ce type de fonctionnalité est appelé document-rémanent, car ces paramètres déterminent directement la manière dont un document est traité.<br/> Fonctionnalité dont les paramètres reflètent les attributs d’appareil physique qui ne sont pas contrôlés par l’utilisateur, tels que la quantité de mémoire dans l’appareil, ou qui indiquent la présence de modules complémentaires facultatifs tels que les alimentations papier ou les duplexeurs. Ce type de fonctionnalité est appelé appareil-rémanent ou imprimante-rémanente. L’état de ce type de fonctionnalité est important, car il peut contraindre une option appartenant à une fonctionnalité rémanente de document.<br/> Une fonctionnalité rémanente d’appareil (rémanente ou d’imprimante) peut être classée comme une fonction d’imprimante (interface utilisateur)-rémanente ou une fonctionnalité d’impression automatique-rémanente. Une fonction d’imprimante-rémanente d’interface utilisateur doit être affichée dans une interface utilisateur qu’un administrateur peut définir. L’appareil détecte automatiquement une fonctionnalité rémanente automatique de l’imprimante.<br/> |
| \*Changer... \* Études<br/>                                                         | Un fournisseur PrintCapabilities doit implémenter une méthode qui crée un document PrintCapabilities qui énumère les fonctionnalités d’impression-rémanente ou de document-rémanent, selon le type spécifié par l’appelant. Pour cette raison, il n’est pas nécessaire de présenter les mêmes informations dans le document PrintCapabilities lui-même.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




