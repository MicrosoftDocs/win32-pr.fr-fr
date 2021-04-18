---
description: Le spouleur d’impression surveille les travaux d’impression en cours et l’imprimante cible pour déterminer le moment approprié pour l’impression d’un travail.
ms.assetid: c3ce7c63-b72d-4e91-9509-5189f2ccac8a
title: Processeur d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bcb7ed062b4e03069201d3ec1faa0ee427f0973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519885"
---
# <a name="print-processor"></a>Processeur d’impression

Le spouleur d’impression surveille les travaux d’impression en cours et l’imprimante cible pour déterminer le moment approprié pour l’impression d’un travail. Une fois que le spouleur a déterminé qu’un travail doit être imprimé, il appelle le processeur d’impression. Le processeur d’impression est un plug-in qui traite les données du travail d’impression.

Utilisez les fonctions suivantes pour travailler avec des processeurs d’impression.



| Fonction                                                           | Description                                                          |
|--------------------------------------------------------------------|----------------------------------------------------------------------|
| [**AddPrintProcessor**](addprintprocessor.md)                     | Installe un processeur d’impression sur un serveur spécifié.                    |
| [**DeletePrintProcessor**](deleteprintprocessor.md)               | Supprime un processeur d’imprimante d’un serveur spécifié.                 |
| [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) | Énumère les types de données pris en charge par un processeur d’impression spécifié. |
| [**EnumPrintProcessors**](enumprintprocessors.md)                 | Énumère les processeurs d’impression installés sur un serveur spécifié.     |
| [**GetPrintProcessorDirectory**](getprintprocessordirectory.md)   | Récupère le chemin d’accès du processeur d’impression sur le serveur spécifié.  |



 

 

 



