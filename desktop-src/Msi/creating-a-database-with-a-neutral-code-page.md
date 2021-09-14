---
description: L’approche recommandée pour gérer les pages de codes consiste à créer une base de données de base neutre qui contient uniquement des caractères qui peuvent être traduits dans une page de codes.
ms.assetid: 8ded41a6-6e5b-4a39-b783-e2b9f83eaed4
title: Création d’une base de données avec une page de codes neutre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08639b6ab3521f183a2dab46dfd257121b28bae0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091901"
---
# <a name="creating-a-database-with-a-neutral-code-page"></a>Création d’une base de données avec une page de codes neutre

L’approche recommandée pour gérer les pages de codes consiste à créer une base de données de base neutre qui contient uniquement des caractères qui peuvent être traduits dans une page de codes. la base de données peut ensuite être définie sur la page de codes de la localisation et les informations de localisation peuvent être ajoutées comme décrit dans [localisation d’un Windows Installer Package](localizing-a-windows-installer-package.md).

Pour créer une base de données neutre, évitez les caractères étendus qui n’appartiennent pas au jeu de caractères ASCII et nécessitent donc une page de codes spéciale. Par exemple, le signe de copyright, le © et le signe de marque déposée,, ne sont pas des caractères ASCII et nécessitent une page de codes ANSI spéciale pour un affichage correct. Utilisez à la place (c) et (r), car ces caractères peuvent être traduits ou transformés en symboles pour la version en anglais. Cette base de données neutre peut ensuite être localisée en définissant sa page de codes et en ajoutant des informations de localisation par modification de table ou en important des fichiers d’archive de texte.

 

 



