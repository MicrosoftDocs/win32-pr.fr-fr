---
description: La date et l’heure ms-dos sont des valeurs compactes 16 bits qui spécifient le mois, le jour, l’année et l’heure de la dernière écriture dans un fichier MS-DOS.
ms.assetid: 948e6d77-dd01-4c90-9ef0-af143972c3fa
title: Date et heure MS-DOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d401c731c9a3f5127511e28adf846c929a89a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517546"
---
# <a name="ms-dos-date-and-time"></a>Date et heure MS-DOS

La **Date** et l' **heure** ms-dos sont des valeurs compactes 16 bits qui spécifient le mois, le jour, l’année et l’heure de la dernière écriture dans un fichier MS-DOS. MS-DOS enregistre la date et l’heure à chaque fois qu’une application MS-DOS crée ou écrit dans un fichier. Les applications MS-DOS récupèrent cette date et cette heure à l’aide des fonctions MS-DOS. Lorsque vous utilisez la fonction [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) pour récupérer les heures de fichier des fichiers qui ont été créés par MS-DOS, **GetFileTime** convertit automatiquement les dates et heures ms-dos en heures UTC.

Si vous rencontrez une date et une heure MS-DOS qui n’ont pas été converties, vous pouvez les convertir en heure UTC à l’aide de la fonction [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) . Cette fonction copie la date et l’heure converties dans une structure [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) . Vous pouvez reconvertir la valeur en date et heure MS-DOS à l’aide de la fonction [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) .

 

 
