---
description: Avant de pouvoir utiliser un journal de fichiers, vous devez appeler SetupInitializeFileLog pour l’ouvrir ou le créer. Lorsque vous appelez cette fonction, vous pouvez spécifier des indicateurs pour créer ou remplacer un journal de fichier, ouvrir le journal système ou ouvrir un journal de fichiers en lecture seule.
ms.assetid: 7ab133f6-2088-4bca-bf24-d3dcb29376a1
title: Utilisation du journal des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf7f1e3d27ba7d42d448a1eac48d60246c2b40db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953246"
---
# <a name="using-the-file-log"></a><span data-ttu-id="68c95-104">Utilisation du journal des fichiers</span><span class="sxs-lookup"><span data-stu-id="68c95-104">Using the File Log</span></span>

<span data-ttu-id="68c95-105">Avant de pouvoir utiliser un journal de fichiers, vous devez appeler [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) pour l’ouvrir ou le créer.</span><span class="sxs-lookup"><span data-stu-id="68c95-105">Before you can use a file log, you must call [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) to open or create it.</span></span> <span data-ttu-id="68c95-106">Lorsque vous appelez cette fonction, vous pouvez spécifier des indicateurs pour créer ou remplacer un journal de fichier, ouvrir le journal système ou ouvrir un journal de fichiers en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="68c95-106">When you call this function, you can specify flags to create or overwrite a file log, open the system log, or open a file log as read-only.</span></span>

<span data-ttu-id="68c95-107">Une fois que [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) a retourné un handle à un fichier journal, vous pouvez ajouter une entrée en appelant [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea), supprimer une entrée en appelant [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)ou récupérer des informations sur un fichier particulier dans un journal de fichier en appelant [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).</span><span class="sxs-lookup"><span data-stu-id="68c95-107">After [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) returns a handle to a file log, you can add an entry by calling [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea), delete an entry by calling [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya), or retrieve information about a particular file in a file log by calling [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).</span></span>

<span data-ttu-id="68c95-108">Lorsque le journal de fichier n’est plus nécessaire, [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) doit être appelé pour libérer les ressources allouées pendant l’appel à [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).</span><span class="sxs-lookup"><span data-stu-id="68c95-108">When the file log is no longer needed, [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) should be called to release the resources allocated during the call to [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).</span></span>

 

 



