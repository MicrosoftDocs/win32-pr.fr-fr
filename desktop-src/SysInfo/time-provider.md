---
description: Le système d’exploitation Microsoft Windows prend en charge un large éventail de périphériques matériels et de protocoles de temps réseau à l’aide de l’architecture du fournisseur de temps.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Fournisseur de temps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c844e2c4d0d49e87e978a47621338b167c4f5a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867381"
---
# <a name="time-provider"></a>Fournisseur de temps

Le système d’exploitation Microsoft Windows prend en charge un large éventail de périphériques matériels et de protocoles de temps réseau à l’aide de l’architecture du *fournisseur de temps* . Les fournisseurs de temps d’entrée récupèrent des horodatages précis à partir du matériel ou du réseau, et les fournisseurs de temps de sortie fournissent des horodateurs à d’autres clients sur le réseau.

Les fournisseurs de temps sont gérés par le *Gestionnaire du fournisseur de temps*. Il est responsable du chargement, du démarrage et de l’arrêt des fournisseurs de temps comme indiqué par le gestionnaire de contrôle des services. Cette interface rend l’écriture d’un fournisseur de temps plus facile que l’écriture d’un service complet.

-   [Création d’un fournisseur de temps](creating-a-time-provider.md)
-   [Inscription d’un fournisseur de temps](registering-a-time-provider.md)
-   [Exemple de fournisseur de temps](sample-time-provider.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Service de temps Windows](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



