---
title: Barre de langue (applications TSF)
description: Une application ne peut pas ajouter d’éléments à la barre de langue ; seul un service de texte peut ajouter des éléments à la barre de langue.
ms.assetid: facb0da1-3f80-4745-b021-c026e7e5356c
keywords:
- Text Services Framework (TSF), barre de langue
- TSF (Text Services Framework), barre de langue
- Applications compatibles TSF, barre de langue
- barre de langue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f0adeacdfe105700efba761b0622432f4ac382d147bd82145242be9fdd71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952107"
---
# <a name="language-bar-tsf-applications"></a>Barre de langue (applications TSF)

Une application ne peut pas ajouter d’éléments à la barre de langue ; seul un service de texte peut ajouter des éléments à la barre de langue. Une application peut avoir un impact sur l’affichage de certains éléments de la barre de langue.

Le [compartiment \_ \_ \_ DICTATIONSTAT de reconnaissance vocale des compartiments GUID](predefined-compartments.md) est utilisé pour indiquer le type d’entrée vocale que l’application peut accepter : entrée de texte directe (dictée) et/ou commandes vocales. Par défaut, la dictée est activée et la commande vocale est désactivée. Si l’application peut accepter des commandes vocales, elle doit définir la valeur d' [ \_ \_ activation](speech-recognition-constants.md) des commandes TF dans le \_ \_ compartiment DICTATIONSTAT de la reconnaissance vocale des GUID \_ . Si l’application peut accepter la dictée, elle doit définir la \_ valeur de la dictée TF \_ activée dans le \_ \_ \_ compartiment DICTATIONSTAT. La \_ dictée TF \_ on ou TF \_ \_ sur la valeur de ce compartiment détermine l’entrée vocale en mode (dictée ou commande) en cours.

Si l’application prend en charge le stockage persistant des données de propriété, elle doit définir le compartiment [ \_ \_ PERSISTMENUENABLED du compartiment GUID](predefined-compartments.md) sur une valeur différente de zéro. Le service de texte vocal active alors l’élément de menu **enregistrer les données vocales** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment configurer Text Services Framework](how-to-set-up-tsf.md)
</dt> <dt>

[Barre de langue (services de texte)](language-bar.md)
</dt> </dl>

 

 




