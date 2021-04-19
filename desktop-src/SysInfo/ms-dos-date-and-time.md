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
# <a name="ms-dos-date-and-time"></a><span data-ttu-id="069d7-103">Date et heure MS-DOS</span><span class="sxs-lookup"><span data-stu-id="069d7-103">MS-DOS Date and Time</span></span>

<span data-ttu-id="069d7-104">La **Date** et l' **heure** ms-dos sont des valeurs compactes 16 bits qui spécifient le mois, le jour, l’année et l’heure de la dernière écriture dans un fichier MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="069d7-104">**MS-DOS date** and **MS-DOS time** are packed 16-bit values that specify the month, day, year, and time of day an MS-DOS file was last written to.</span></span> <span data-ttu-id="069d7-105">MS-DOS enregistre la date et l’heure à chaque fois qu’une application MS-DOS crée ou écrit dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="069d7-105">MS-DOS records the date and time whenever an MS-DOS application creates or writes to a file.</span></span> <span data-ttu-id="069d7-106">Les applications MS-DOS récupèrent cette date et cette heure à l’aide des fonctions MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="069d7-106">MS-DOS applications retrieve this date and time using MS-DOS functions.</span></span> <span data-ttu-id="069d7-107">Lorsque vous utilisez la fonction [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) pour récupérer les heures de fichier des fichiers qui ont été créés par MS-DOS, **GetFileTime** convertit automatiquement les dates et heures ms-dos en heures UTC.</span><span class="sxs-lookup"><span data-stu-id="069d7-107">When you use the [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) function to retrieve the file times for files that were created by MS-DOS, **GetFileTime** automatically converts MS-DOS dates and times to UTC-based times.</span></span>

<span data-ttu-id="069d7-108">Si vous rencontrez une date et une heure MS-DOS qui n’ont pas été converties, vous pouvez les convertir en heure UTC à l’aide de la fonction [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) .</span><span class="sxs-lookup"><span data-stu-id="069d7-108">If you encounter an MS-DOS date and time that has not been converted, you can convert it to a UTC-based time by using the [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) function.</span></span> <span data-ttu-id="069d7-109">Cette fonction copie la date et l’heure converties dans une structure [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="069d7-109">This function copies the converted date and time to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span> <span data-ttu-id="069d7-110">Vous pouvez reconvertir la valeur en date et heure MS-DOS à l’aide de la fonction [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) .</span><span class="sxs-lookup"><span data-stu-id="069d7-110">You can convert the value back to an MS-DOS date and time by using the [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) function.</span></span>

 

 
