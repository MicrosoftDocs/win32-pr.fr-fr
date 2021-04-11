---
description: Processus d’allocation des ressources du distributeur de ressources
ms.assetid: 695d08f4-ba5c-4a5f-a2ad-481a8ede49ab
title: Processus d’allocation des ressources du distributeur de ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a12cb22abd6d4d825f1ca048495b032a77fe216
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200978"
---
# <a name="resource-dispenser-resource-allocation-process"></a>Processus d’allocation des ressources du distributeur de ressources

Chaque fois qu’un distributeur de ressources alloue une ressource de son détenteur, voici ce qui se produit :

1.  Le distributeur de ressources déclare un identificateur de type de ressource (**RESTYPID**), qui décrit le type de ressource requis.

2.  Le distributeur de ressources appelle la méthode [**IHolder :: AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) du détenteur, en passant ce **RESTYPID**.

3.  Le détenteur génère une liste de candidats à partir des ressources disponibles. Les candidats sont des ressources qui ne sont pas inscrites dans une transaction ou déjà inscrites dans la transaction de l’objet appelant.

4.  Ces candidats sont passés individuellement à la méthode [**IDispenserDriver :: RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) , où ils sont évalués (sur une échelle de 0 à 100) en fonction de la correspondance entre la ressource candidate et le **RESTYPID** souhaité.

5.  Le détenteur choisit la ressource dont le distributeur de ressources est le plus élevé.

6.  Le distributeur de ressources peut mettre fin à la boucle d’évaluation dès le début en affectant au candidat une évaluation de la ressource 100 (un ajustement parfait). Une évaluation de 100 serait normalement réservée pour les ressources candidates qui sont déjà inscrites, sauf si le distributeur de ressources conclut que l’inscription est une opération peu coûteuse. Si toutes les ressources candidates (le cas échéant) sont évaluées à 0 (inutilisables), une nouvelle ressource est créée en appelant [**IDispenserDriver :: CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).

7.  Si la ressource choisie précédemment n’est pas déjà inscrite dans la transaction de l’objet appelant, la méthode [**IDispenserDriver :: EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) du distributeur de ressources est appelée.

8.  L’appel de la méthode [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) retourne au distributeur de ressources avec la ressource inscrite.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts du distributeur de ressources COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Inscription d’une ressource dans une transaction](enlisting-a-resource-in-a-transaction.md)
</dt> <dt>

[Suivi des ressources non allouées](tracking-non-allocated-resources.md)
</dt> </dl>

 

 



