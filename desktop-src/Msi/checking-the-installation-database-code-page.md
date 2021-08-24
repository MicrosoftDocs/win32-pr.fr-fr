---
description: Une page de codes est une table interne que le système d’exploitation utilise pour mapper des symboles (lettres, chiffres et signes de ponctuation) à un nombre de caractères.
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: Vérification de la page de codes de la base de données d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cedb63128d4a3b18878eba16af5e55da92403953ddf2a2c9a29c788a524ad41f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581769"
---
# <a name="checking-the-installation-database-code-page"></a>Vérification de la page de codes de la base de données d’installation

Une *page de codes* est une table interne que le système d’exploitation utilise pour mapper des symboles (lettres, chiffres et signes de ponctuation) à un nombre de caractères. Différentes pages de codes assurent la prise en charge des jeux de caractères utilisés dans différents pays ou régions. Les pages de codes sont référencées par nombre ; par exemple, la page de codes 932 représente le jeu de caractères japonais, et la page de codes 950 représente l’un des jeux de caractères chinois. Consultez [localisation des tables Error et ActionText](localizing-the-error-and-actiontext-tables.md) pour obtenir la liste des pages de codes ASCII.

La même page de codes ASCII, 1252, peut être utilisée pour l’anglais et le français. Par conséquent, la page de codes de la MNP2000.msi de base de données (anglais) n’a pas besoin d’être réinitialisée pour modifier l’installation en français.

pour plus d’informations sur la définition de la page de codes [, consultez gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md).

[Continuer](importing-localized-error-and-actiontext-tables.md)

 

 



