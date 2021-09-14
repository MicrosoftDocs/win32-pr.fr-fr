---
description: Objets de fournisseur de matériel
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: Objets de fournisseur de matériel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1aaebf61e97487b48a6b8bf0dbd91cc6aa3e0bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856485"
---
# <a name="hardware-provider-objects"></a>Objets de fournisseur de matériel

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Le modèle d’objet VDS comprend un ensemble d’objets pour interroger et configurer des entités de fournisseur de matériel. (Notez que bien que VDS comprenne un fournisseur de logiciels, vous devez acheter un fournisseur de matériel et le matériel associé séparément pour tirer parti des objets de fournisseur de matériel.) Ces objets de fournisseur de matériel représentent des appareils physiques (tels que des sous-systèmes, des lecteurs et des contrôleurs) et des périphériques virtuels (tels que les LUN et les plex de LUN).

Un fournisseur de matériel doit créer un objet COM pour chaque appareil physique ou virtuel.

L’illustration qui suit montre la relation entre l’objet fournisseur et le jeu d’objets de fournisseur de matériel, ainsi que la relation entre les différents objets de fournisseur de matériel eux-mêmes.

![Diagramme qui montre la relation entre le « fournisseur » et le « sous-système », le « contrôleur », le numéro d’unité logique, le « LUN Plex », le « lecteur » et le « fuseau ». ](images/vdshwobjects.png)

Un objet fournisseur peut contenir un nombre quelconque de sous-systèmes. Tous les fournisseurs de matériel peuvent gérer plusieurs instances du même modèle de sous-système. De nombreux fournisseurs de matériel peuvent également gérer plusieurs instances de différents modèles de sous-système. Un même ordinateur peut héberger un nombre quelconque de fournisseurs de matériel.

Un objet sous-système peut contenir un nombre quelconque de contrôleurs et de lecteurs, et peut surfacer un nombre quelconque de numéros d’unités logiques. Un objet LUN comprend au moins un plex LUN, et chaque Plex LUN est mappé à un ou plusieurs lecteurs, selon le type de plex. Les objets de contrôleur peuvent gérer l’entrée/sortie de données pour un nombre quelconque d’objets LUN.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle d’objet VDS](vds-object-model.md)
</dt> </dl>

 

 
