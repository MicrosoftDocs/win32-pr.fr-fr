---
description: Cette section décrit la syntaxe et l’utilisation de la gestion structurée des exceptions telle qu’elle est implémentée dans le compilateur d’optimisation Microsoft C/C++. Les mots clés suivants sont interprétés par le compilateur dans le cadre du mécanisme de gestion structurée des exceptions.
ms.assetid: 22190b75-417c-49d3-83fe-546018fb61ea
title: Syntaxe du gestionnaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5171a1de095faa0c3362a7998903d31f90eb630e51c5ec16e7e77d467117715c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260609"
---
# <a name="handler-syntax"></a>Syntaxe du gestionnaire

Cette section décrit la syntaxe et l’utilisation de la gestion structurée des exceptions telle qu’elle est implémentée dans le compilateur d’optimisation Microsoft C/C++. Les mots clés suivants sont interprétés par le compilateur dans le cadre du mécanisme de gestion structurée des exceptions.



| Mot clé         | Description                                                                                                                                                                                                                                      |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_\_Essayez**     | Commence un corps de code protégé. Utilisé avec le mot clé **\_ \_ except** pour construire un [Gestionnaire d’exceptions](exception-handler-syntax.md), ou avec le mot clé **\_ \_ finally** pour construire un gestionnaire de [terminaisons](termination-handler-syntax.md). |
| **\_\_mais**  | Commence un bloc de code qui est exécuté uniquement lorsqu’une exception se produit dans son bloc **\_ \_ try** associé.                                                                                                                                   |
| **\_\_suivie** | Commence un bloc de code qui est exécuté chaque fois que le workflow de contrôle quitte son bloc **\_ \_ try** associé.                                                                                                                                    |
| **\_\_congé**   | Autorise l’arrêt immédiat du bloc **\_ \_ try** sans entraîner un arrêt anormal et une baisse des performances.                                                                                                                      |



 

Le compilateur interprète également les fonctions [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md)et [**AbnormalTermination**](abnormaltermination.md) comme des mots clés, et leur utilisation en dehors de la syntaxe de gestion des exceptions appropriée génère une erreur du compilateur. Vous trouverez ci-dessous une brève description de ces fonctions.



| Fonction                                                   | Description                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExceptionCode**](getexceptioncode.md)               | Retourne un code qui identifie le type d’exception. Cette fonction ne peut être appelée qu’à partir de l’expression de filtre ou du bloc de gestionnaire d’exceptions.                                                                                                |
| [**GetExceptionInformation**](getexceptioninformation.md) | Retourne un pointeur vers une structure de [**\_ pointeurs d’exception**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) contenant des pointeurs vers l’enregistrement de contexte et l’enregistrement d’exception. Cette fonction ne peut être appelée qu’à partir de l’expression de filtre d’un gestionnaire d’exceptions. |
| [**AbnormalTermination**](abnormaltermination.md)         | Indique si le workflow de contrôle a quitté le bloc **\_ \_ try** associé de manière séquentielle après l’exécution de la dernière instruction dans le bloc. Cette fonction ne peut être appelée qu’à partir du bloc **\_ \_ finally** d’un gestionnaire de terminaisons.              |



 

 

 



