---
title: Philosophie de conception des files d’attente de commandes et des listes de commandes
description: Les objectifs de la réutilisation du travail de rendu et de la mise à l’échelle multithread requièrent des modifications fondamentales à la façon dont les applications Direct3D soumettent le rendu du travail au GPU.
ms.assetid: C85C8C41-2306-4568-8FAE-F57EDA624298
keywords:
- Liste des commandes
- bundle
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812275a630464dbe9137d587a672803f4d0c72f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293603"
---
# <a name="design-philosophy-of-command-queues-and-command-lists"></a>Philosophie de conception des files d’attente de commandes et des listes de commandes

Les objectifs de la réutilisation du travail de rendu et de la mise à l’échelle multithread requièrent des modifications fondamentales à la façon dont les applications Direct3D soumettent le rendu du travail au GPU. Dans Direct3D 12, le processus d’envoi du travail de rendu diffère des versions antérieures de trois façons importantes :

<dl> 1. Élimination du contexte immédiat. Cela permet l’activation de plusieurs threads.  
2. Les applications possèdent désormais la manière dont les appels de rendu sont regroupés dans les éléments de travail de l’unité de traitement graphique (GPU). Cela permet la réutilisation.  
3. Les applications contrôlent désormais explicitement le moment où le travail est soumis au GPU. Cela permet d’activer les éléments 1 et 2.  
</dl>

-   [Suppression du contexte immédiat](#removal-of-the-immediate-context)
-   [Regroupement d’éléments de travail GPU](#grouping-of-gpu-work-items)
-   [Envoi de travail GPU](#gpu-work-submission)
-   [Rubriques connexes](#related-topics)

## <a name="removal-of-the-immediate-context"></a>Suppression du contexte immédiat

La plus grande modification entre Microsoft Direct3D 11 et Microsoft Direct3D 12 est qu’il n’y a plus de contexte unique et immédiat associé à un appareil. Au lieu de cela, pour le rendu, les applications créent des listes de commandes dans lesquelles les API de rendu traditionnelles peuvent être appelées. Une liste de commandes ressemble à la méthode Render d’une application Direct3D 11 qui utilisait le contexte immédiat, car elle contient des appels qui dessinent des primitives ou modifient l’état de rendu. À l’instar des contextes immédiats, chaque liste de commandes n’est pas à thread libre ; Toutefois, plusieurs listes de commandes peuvent être enregistrées simultanément, ce qui tire parti des processeurs multicœurs modernes.

Les listes de commandes sont généralement exécutées une seule fois. Toutefois, une liste de commandes peut être exécutée plusieurs fois si l’application s’assure que les exécutions précédentes sont terminées avant d’envoyer de nouvelles exécutions. Pour plus d’informations sur la synchronisation de la liste de commandes, consultez [exécution et synchronisation de listes de commandes](executing-and-synchronizing-command-lists.md).

## <a name="grouping-of-gpu-work-items"></a>Regroupement d’éléments de travail GPU

En plus des listes de commandes, Direct3D 12 tire parti des fonctionnalités présentes dans tout le matériel dès aujourd’hui en ajoutant un second niveau de listes de commandes, appelées « *bottes*». Pour vous aider à distinguer ces deux types, les listes de commandes de premier niveau peuvent être appelées *listes de commandes directes*. L’objectif des offres groupées est de permettre aux applications de regrouper un petit nombre de commandes API pour une exécution ultérieure et répétée à partir de listes de commandes directes. Au moment de la création d’un bundle, le pilote effectue le plus grand traitement possible pour une exécution ultérieure. Les lots peuvent ensuite être exécutés à partir de plusieurs listes de commandes et plusieurs fois dans la même liste de commandes.

La réutilisation des offres groupées est un gros pilote d’efficacité améliorée avec les threads d’UC uniques. Étant donné que les offres groupées sont prétraitées et peuvent être envoyées plusieurs fois, il existe certaines restrictions sur les opérations pouvant être effectuées au sein d’un regroupement. Pour plus d’informations, consultez [création et enregistrement des listes de commandes et des offres groupées](recording-command-lists-and-bundles.md).

## <a name="gpu-work-submission"></a>Envoi de travail GPU

Pour exécuter le travail sur le GPU, une application doit envoyer explicitement une liste de commandes à une file d’attente de commandes associée à l’appareil Direct3D. Une liste de commandes directe peut être soumise à plusieurs reprises pour exécution, mais l’application est chargée de s’assurer que la liste de commandes directe a fini de s’exécuter sur le GPU avant de la soumettre à nouveau. Les offres groupées n’ont pas de restrictions d’utilisation simultanée et peuvent être exécutées plusieurs fois dans plusieurs listes de commandes, mais elles ne peuvent pas être envoyées directement à une file d’attente de commandes en vue de leur exécution.

Tout thread peut envoyer une liste de commandes à n’importe quelle file d’attente de commandes à tout moment, et le runtime sérialise automatiquement la soumission de la liste de commandes dans la file d’attente de commandes tout en préservant l’ordre d’envoi.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Envoi de travail dans Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

 




