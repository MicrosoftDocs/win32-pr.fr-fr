---
description: Journalisation des erreurs
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: Journalisation des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7402ade284f0d9a71b032f233276277dfdcd8c5e2844c85f03782caed101d095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685149"
---
# <a name="logging-errors"></a>Journalisation des erreurs

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

les [Services d’édition de DirectShow](directshow-editing-services.md) fournissent un mécanisme intégré pour la journalisation des erreurs qui se produisent lors du chargement, de la construction ou du rendu d’un projet DES. Cet article présente un exemple d’application console qui charge un fichier de projet XML et tente de l’afficher. Si une erreur se produit, l’application imprime un message d’erreur dans la fenêtre de console. L’exemple de code présenté dans cet article s’appuie sur l’exemple donné lors [du chargement et de l’aperçu d’un Project](loading-and-previewing-a-project.md).

> [!Note]  
> Votre application n’est pas obligée d’implémenter la journalisation des erreurs. DES n’enregistre pas d’erreurs, sauf si vous le demandez explicitement.

 

Cet article suppose que vous comprenez la programmation du client COM et le modèle de chronologie DES. En outre, vous devez comprendre les principes fondamentaux de la programmation d’objets COM. Pour plus d’informations sur les chronologies dans DES, consultez [le modèle Timeline](the-timeline-model.md).

Cet article contient les sections suivantes.

-   [Vue d’ensemble de la journalisation des erreurs](overview-of-error-logging.md)
-   [Création d’une classe de journalisation des erreurs](creating-an-error-logging-class.md)
-   [Implémentation de IAMErrorLog](implementing-iamerrorlog.md)
-   [Définition du journal des erreurs](setting-the-error-log.md)
-   [Journal DES Erreurs DES : exemple de code](des-error-logging--example-code.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[utilisation des Services de modification DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



