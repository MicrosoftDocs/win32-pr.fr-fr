---
title: Interfaces DO
description: Utilisez les interfaces d’optimisation de remise suivantes pour transférer des fichiers et surveiller des travaux dans la file d’attente de transfert.
ms.assetid: 20203CCD-86CC-4551-BA4F-0A5999F8C956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0359328f189c1a5b5d9649d8300dc59a80df4480
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106538996"
---
# <a name="do-interfaces"></a>Interfaces DO

Utilisez les interfaces d’optimisation de remise suivantes pour transférer des fichiers et surveiller des travaux dans la file d’attente de transfert.

| Interface | Description |
|-|-|
| [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) | Les clients implémentent l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) pour recevoir une notification indiquant qu’un travail est terminé, a été modifié ou est erroné. |
| [**IBackgroundCopyError**](ibackgroundcopyerror.md) | Récupère les détails d’une erreur de tâche. |
| [**IBackgroundCopyFile**](ibackgroundcopyfile.md) | Récupère les noms de fichiers locaux et distants d’une demande de transfert de fichiers dans le travail et de sa progression. |
| [**IBackgroundCopyFile2**](ibackgroundcopyfile2.md) | Spécifie un nouveau nom distant pour le fichier et récupère la liste des plages à télécharger. |
| [**IBackgroundCopyFile5**](ibackgroundcopyfile5.md) | Fournit des méthodes d’extraction et de définition de propriétés génériques pour les propriétés BackgroundCopyFile. |
| [**Méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md) | Ajoute des fichiers au travail, définit le niveau de priorité du travail, détermine l’état du travail et démarre et arrête le travail. |
| [**IBackgroundCopyJob5**](ibackgroundcopyjob5.md) | Interroge ou définit plusieurs comportements facultatifs d’un travail. |
| [**IBackgroundCopyManager**](ibackgroundcopymanager.md) | Crée des tâches de transfert, extrait un objet énumérateur de travaux dans la file d’attente et récupère des tâches individuelles de la file d’attente. |
| [**IDeliveryOptimizationJob**](ideliveryoptimizationjob.md) | Utilisez pour télécharger des plages d’un fichier. |
| [**IDeliveryOptimizationFile**](ideliveryoptimizationfile.md) | Permet d’identifier l’état d’un fichier spécifique. |
| [**IDODownload**](./do/nn-do-idodownload.md) | Utilisé pour démarrer et gérer un téléchargement. |
| [**IDODownloadInternal**](./dodownloadinternal/nn-dodownloadinternal-idodownloadinternal.md) | Utilisé pour récupérer ou définir les propriétés de téléchargement étendues. |
| [**IDODownloadStatusCallback**](./do/nn-do-idodownloadstatuscallback.md) | Utilisé pour recevoir des notifications relatives à un téléchargement. |
| [**IDOManager**](./do/nn-do-idomanager.md) | Utilisé pour créer un nouveau téléchargement et énumérer les téléchargements existants. |
| [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) | Énumère les fichiers du travail. |