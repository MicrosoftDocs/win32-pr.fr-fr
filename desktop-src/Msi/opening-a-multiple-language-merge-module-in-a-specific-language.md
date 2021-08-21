---
description: Lors de la fusion d’un module dans une base de données d’installation, il existe deux langues importantes.
ms.assetid: e815854f-a379-497a-ae37-b13de39dd516
title: Ouverture d’un module de fusion Multiple-Language dans un langage spécifique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4dd46009f0cbe4f8c0f2cfd8b4f5dcd2caf91c7987ece7b3b032f61d9161ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942870"
---
# <a name="opening-a-multiple-language-merge-module-in-a-specific-language"></a>Ouverture d’un module de fusion Multiple-Language dans un langage spécifique

Lors de la fusion d’un module dans une base de données d’installation, il existe deux langues importantes. La première est la langue du package d’installation cible spécifié par [**ProductLanguage**](productlanguage.md) dans la [table des propriétés](property-table.md). La seconde est la langue du module de fusion qui apparaît dans la colonne Language de la [table ModuleSignature](modulesignature-table.md).

La langue du package d’installation peut être transmise au module par l’outil de fusion lorsque le package est ouvert pour une fusion. Toutefois, il peut parfois être nécessaire d’ignorer la langue de la cible et de demander que le module soit ouvert dans un autre langage, par exemple, un package en anglais qui installe les ressources en anglais et en allemand à partir du module.

Lors de l’ouverture d’un module à l’aide d’une requête de langue, l’outil de fusion vérifie la langue demandée par rapport aux langues spécifiées dans la colonne Language de la [table ModuleSignature](modulesignature-table.md).

Le processus suivant est utilisé pour déterminer la langue à utiliser.

**Pour déterminer la langue à utiliser**

1.  Si la langue de la [table ModuleSignature](modulesignature-table.md) est égale ou plus générale que la langue demandée, le module s’ouvre.
2.  Si le module prend en charge la langue exacte demandée, cette langue est utilisée.
3.  Si le module prend en charge le groupe de langues de la langue demandée par le groupe de langues, par exemple, cochez 9 si 1033 a été demandé, mais introuvable à l’étape 2.
4.  Vérifiez s’il existe une transformation de langue qui modifie le module en neutre.
5.  Si aucune des étapes précédentes ne réussit, le module ne prend pas en charge la langue demandée et la fusion échoue.

 

 



