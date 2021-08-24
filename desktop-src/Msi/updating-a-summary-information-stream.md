---
description: La valeur de la propriété Résumé du numéro de révision dans le flux d’informations de résumé doit être remplacée par une nouvelle valeur unique lors de la localisation d’une base de données, car la base de données d’installation est en cours de modification. Consultez codes de package.
ms.assetid: fce292c5-6702-4948-a13a-2a9ccacbd5c9
title: Mise à jour d’un flux d’informations de synthèse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d95e6a0cf09af5d4a024f707c0694d89def47abf8f731f394c55a11232bc07f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039279"
---
# <a name="updating-a-summary-information-stream"></a>Mise à jour d’un flux d’informations de synthèse

La valeur de la propriété [**Résumé du numéro de révision**](revision-number-summary.md) dans le flux d’informations de [Résumé](summary-information-stream.md) doit être remplacée par une nouvelle valeur unique lors de la localisation d’une base de données, car la base de données d’installation est en cours de modification. Consultez [codes de package](package-codes.md).

La valeur de la propriété [**Résumé du modèle**](template-summary.md) dans le flux d’informations de résumé doit être remplacée par l’identificateur de langue numérique (LANGID) du nouveau langage.

Si les chaînes de texte descriptives dans le flux d’informations de synthèse sont localisées dans la nouvelle langue, la propriété de résumé de la page de [**codes**](codepage-summary.md) doit être définie sur la page de codes appropriée pour la nouvelle langue.

Vous pouvez modifier le flux d’informations de synthèse du package localisé en procédant de la même façon que lors de l' [Ajout d’informations de résumé](adding-summary-information.md). un exemple illustrant l’utilisation des méthodes d’informations récapitulatives de la base de données est également fourni dans le kit de développement logiciel (SDK) Windows Installer en tant que WiSumInf.vbs de l’utilitaire. Pour plus d’informations sur la WiSumInf.vbs, consultez [gérer les informations de résumé](manage-summary-information.md).

[Continuer](adding-localized-resources.md)

 

 



