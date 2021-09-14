---
description: le service Windows Installer utilise la langue de l’utilisateur actuel dans toutes les boîtes de dialogue jusqu’à l’ouverture d’un package Windows Installer.
ms.assetid: c9902990-7a26-48fd-96ac-4d5a749e34be
title: Localisation de la langue affichée par les boîtes de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042b2b7f9ac256ebad265b75a8756fc422403e37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011942"
---
# <a name="localizing-the-language-displayed-by-dialogs"></a>Localisation de la langue affichée par les boîtes de dialogue

le service Windows Installer utilise la langue de l’utilisateur actuel dans toutes les boîtes de dialogue jusqu’à l’ouverture d’un package Windows Installer. le Windows Installer détermine cela à l’aide de **GetUserDefaultUILanguage**. lors de l’ouverture d’un package Windows Installer, le programme d’installation affiche les boîtes de dialogue à l’aide de la langue du package, comme spécifié par la propriété [**résumé du modèle**](template-summary.md) .

pour plus d’informations sur la localisation du langage d’un package de Windows Installer, consultez également [un exemple de localisation](a-localization-example.md).

 

 



