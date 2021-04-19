---
description: Si vous fournissez des compteurs sur un ordinateur 64 bits, vous devez installer la version 32 bits et 64 bits de votre fournisseur sur l’ordinateur si vous souhaitez prendre en charge les consommateurs 32 bits et 64 bits.
ms.assetid: 2dba2c46-0185-4ce6-a7cc-27cdd9b19b70
title: Support 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e465529f35d8a9becb2583e9d5c00ac19a74d3be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530862"
---
# <a name="64-bit-support"></a>Support 64 bits

Une DLL du fournisseur de données de performances 64 bits ne peut pas s’exécuter dans un processus consommateur 32 bits et une DLL du fournisseur de données de performance 32 bits ne peut pas s’exécuter dans un processus de 64 bits. L’inscription du fournisseur ne prend en charge qu’une seule `Library` valeur pour le chemin d’accès à votre dll de fournisseur de données de performances. vous ne pouvez donc pas fournir différents chemins d’accès à utiliser par les consommateurs 32 bits et les consommateurs de 64 bits.

Les options suivantes sont disponibles pour prendre en charge les fournisseurs v1 sur les systèmes d’exploitation 64 bits :

- **Recommandé :** Installez et enregistrez le chemin d’accès à la version 32 bits de votre DLL de fournisseur.
  - les consommateurs 32 bits fonctionnent en mode natif : ils chargent votre DLL du fournisseur 32 bits dans le processus consommateur 32 bits.
  - les consommateurs 64 bits fonctionnent indirectement : ils ne peuvent pas charger votre DLL du fournisseur 32 bits dans le processus consommateur 64 bits, mais Windows revient automatiquement à la création d’un processus de perfhost 32 bits, au chargement de votre DLL du fournisseur 32 bits dans le processus perfhost et à l’envoi des données de performances du processus perfhost 32 bits vers le processus consommateur 64 bits.
- **64-bit uniquement :** Installez et enregistrez le chemin d’accès à la version 64 bits de votre DLL de fournisseur.
  - les consommateurs 32 bits échouent : ils ne peuvent pas charger votre DLL du fournisseur 64 bits dans le processus 32 bits.
  - les consommateurs 64 bits fonctionnent en mode natif : ils chargent votre DLL du fournisseur 32 bits in-process.

> [!NOTE]
> Plusieurs fournisseurs de données de performances Windows intégrés installent une DLL 32 bits dans `%systemroot%\syswow64` , installent une dll 64 bits dans `%systemroot%\system32` et inscrivent le `Library` chemin d’accès en tant que `%systemroot%\system32\ProviderName.dll` , ce qui permet la redirection du système de fichiers pour résoudre le chemin d’accès à la dll appropriée. Cela est pris en charge uniquement pour les fournisseurs de données de performances qui font partie du système d’exploitation Windows. Les fournisseurs qui ne font pas partie du système d’exploitation Windows ne doivent pas installer les fichiers dans le `Windows` dossier. Les fichiers non reconnus dans le `Windows` dossier peuvent être supprimés pendant la maintenance ou la mise à niveau.
