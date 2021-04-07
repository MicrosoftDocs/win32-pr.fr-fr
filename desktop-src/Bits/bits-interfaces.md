---
title: Interfaces BITS
description: Utilisez les interfaces de Service de transfert intelligent en arrière-plan (BITS) suivantes pour transférer des fichiers et surveiller des travaux dans la file d’attente de transfert.
ms.assetid: 72668c9b-e6f3-4f3f-9d4b-50d930d1889d
ms.topic: article
ms.date: 01/08/2019
ms.openlocfilehash: fc95d4aea6d6d74ff2952cf2ef686fbaa1049732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939670"
---
# <a name="bits-interfaces"></a>Interfaces BITS

Utilisez les interfaces de Service de transfert intelligent en arrière-plan (BITS) suivantes pour [transférer des fichiers et surveiller des travaux](using-bits.md) dans la file d’attente de transfert.

| Interface | Description |
|-|-|
| [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) | Les clients implémentent l’interface [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) pour recevoir une notification indiquant qu’un travail est terminé, a été modifié ou est erroné. |
| [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) | Les clients implémentent l’interface [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) pour recevoir la notification de la fin du téléchargement d’un fichier. |
| [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) | Les clients implémentent l’interface [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) pour recevoir une notification indiquant que les plages d’un fichier ont été téléchargées. |
| [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) | Récupère les détails d’une erreur de tâche. |
| [**IBackgroundCopyFile**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyfile) | Récupère les noms de fichiers locaux et distants d’une demande de transfert de fichiers dans le travail et de sa progression. |
| [**IBackgroundCopyFile2**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2) | Spécifie un nouveau nom distant pour le fichier et récupère la liste des plages à télécharger. |
| [**IBackgroundCopyFile3**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3) | Valide le fichier de sorte que les pairs puissent demander son contenu et récupère le nom du fichier temporaire. |
| [**IBackgroundCopyFile4**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4) | Récupère les statistiques de téléchargement pour les homologues et les serveurs d’origine. |
| [**IBackgroundCopyFile5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5) | Fournit des méthodes d’extraction et de définition de propriétés génériques pour les propriétés BackgroundCopyFile. |
| [**IBackgroundCopyFile6**](/windows/desktop/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6) | Obtient ou définit les propriétés génériques des transferts de fichiers BITS. |
| [**Méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) | Ajoute des fichiers au travail, définit le niveau de priorité du travail, détermine l’état du travail et démarre et arrête le travail. |
| [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) | Récupère les données de réponse d’un travail de chargement, détermine la progression du transfert des données de réponse au client, demande l’exécution de la ligne de commande et fournit les informations d’identification d’un proxy et d’un serveur distant. |
| [**IBackgroundCopyJob3**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3) | Télécharge les plages d’un fichier, modifie le préfixe d’un nom de fichier distant et conserve les informations de propriétaire et de liste de contrôle d’accès avec le fichier. |
| [**IBackgroundCopyJob4**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4) | Active la mise en cache d’homologue, limite le temps de téléchargement et inspecter les caractéristiques des jetons utilisateur. |
| [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) | Interroge ou définit plusieurs comportements facultatifs d’un travail. |
| [**IBackgroundCopyJobHttpOptions**](/windows/desktop/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions) | Spécifie les certificats clients pour l’authentification du client basée sur les certificats et les en-têtes personnalisés pour les requêtes HTTP. |
| [**IBackgroundCopyJobHttpOptions2**](/windows/desktop/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2) | Utilisez cette interface pour récupérer et/ou pour remplacer la méthode HTTP utilisée pour un transfert BITS. |
| [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) | Crée des tâches de transfert, extrait un objet énumérateur de travaux dans la file d’attente et récupère des tâches individuelles de la file d’attente. |
| [**IBitsPeer**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeer) | Obtient des informations sur un homologue dans le voisinage. |
| [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) | Gérez le pool d’homologues à partir duquel vous pouvez télécharger du contenu. |
| [**IBitsPeerCacheRecord**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacherecord) | Obtient des informations sur un fichier dans le cache. |
| [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) | Associe et gère une paire de jetons de sécurité pour une tâche de transfert Service de transfert intelligent en arrière-plan (BITS). |
| [**IEnumBackgroundCopyFiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) | Énumère les fichiers du travail. |
| [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) | Énumère les travaux dans la file d’attente de transfert. |
| [**IEnumBitsPeerCacheRecords**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords) | Énumère les enregistrements du cache. |
| [**IEnumBitsPeers**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeers) | Énumère la liste des homologues détectés par BITS. |



 

 

 




