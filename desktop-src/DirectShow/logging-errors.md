---
description: Journalisation des erreurs
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: Journalisation des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76cded9d4cfaedd93e846fec52b07bf5d4eef9a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745972"
---
# <a name="logging-errors"></a>Journalisation des erreurs

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Les [services de modification DirectShow](directshow-editing-services.md) (des) fournissent un mécanisme intégré pour la journalisation des erreurs qui se produisent lors du chargement, de la construction ou du rendu d’un projet des. Cet article présente un exemple d’application console qui charge un fichier de projet XML et tente de l’afficher. Si une erreur se produit, l’application imprime un message d’erreur dans la fenêtre de console. L’exemple de code présenté dans cet article s’appuie sur l’exemple donné lors [du chargement et de l’aperçu d’un projet](loading-and-previewing-a-project.md).

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

[Utilisation des services de modification DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



