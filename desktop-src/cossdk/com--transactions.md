---
description: Transactions COM+
ms.assetid: 40eccce1-a362-4adc-8060-f6923b9162c9
title: Transactions COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef51f4c8ed5e37101f64d36af385c93ac7e69ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393132"
---
# <a name="com-transactions"></a>Transactions COM+

Lorsque vous achetez un livre à partir d’une librairie en ligne, vous utilisez une carte de crédit pour commercialiser un livre. Une fois que vous avez envoyé votre commande, une série d’opérations connexes (validation de votre carte de crédit, vérification de la disponibilité de l’inventaire, etc.) vous permet d’obtenir le livre et de faire en sorte que la librairie récupère votre argent. Si une seule opération de la série échoue pendant l’échange, la totalité de l’échange échoue. Vous n’avez pas obtenu le livre et la librairie n’obtient pas votre argent.

La technologie chargée de rendre cet échange en ligne équilibré et prévisible est appelée *traitement des transactions*. Par programme, une *transaction* est une unité de travail dans laquelle une série d’opérations se produisent. COM+ utilise des transactions de programmation pour s’assurer que les ressources ne sont pas mises à jour de façon permanente, à moins que toutes les opérations dans la transaction se terminent correctement En liant un ensemble d’opérations connexes dans une transaction COM+ qui réussit complètement ou échoue, vous pouvez grandement simplifier la récupération des erreurs.

Les rubriques suivantes présentent la théorie générale du traitement des transactions, fournissent un examen approfondi des transactions dans COM+ et présentent des conseils pratiques pour l’écriture de composants transactionnels.



| Rubrique                                                                   | Description                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Concepts des transactions COM+](com--transactions-concepts.md)<br/> | Présente les termes et les concepts de base.<br/>                                  |
| [Tâches des transactions COM+](com--transactions-tasks.md)<br/>       | Fournit des informations pratiques sur l’écriture de composants transactionnels.<br/> |



 

 

 




