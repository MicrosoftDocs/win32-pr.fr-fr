---
description: Les rédacteurs et les demandeurs maintiennent les informations nécessaires à une opération de sauvegarde ou de restauration dans leurs propres documents de métadonnées.
ms.assetid: 1ce56374-cfbf-4ee4-b942-8a7391911a38
title: Métadonnées VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e718d3fb0290f8610944180c079e4d615124eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533600"
---
# <a name="vss-metadata"></a><span data-ttu-id="6d76d-103">Métadonnées VSS</span><span class="sxs-lookup"><span data-stu-id="6d76d-103">VSS Metadata</span></span>

<span data-ttu-id="6d76d-104">Les rédacteurs et les demandeurs maintiennent les informations nécessaires à une opération de sauvegarde ou de restauration dans leurs propres documents de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="6d76d-104">Both writers and requesters maintain information necessary to a backup or restore operation in their own metadata documents.</span></span>

<span data-ttu-id="6d76d-105">Ces documents, respectivement le [*document de métadonnées*](vssgloss-w.md) de l’enregistreur et le [*document composants de sauvegarde*](vssgloss-b.md), sont utilisés comme base pour la communication et la coordination des rédacteurs et des demandeurs pendant les activités de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="6d76d-105">These documents, the [*Writer Metadata Document*](vssgloss-w.md) and the [*Backup Components Document*](vssgloss-b.md), respectively, are used as the basis for writer and requester communication and coordination during backup and restore activities.</span></span>

<span data-ttu-id="6d76d-106">Les métadonnées sont représentées au format XML à l’aide d’un schéma propriétaire.</span><span class="sxs-lookup"><span data-stu-id="6d76d-106">The metadata is represented in XML format using a proprietary schema.</span></span> <span data-ttu-id="6d76d-107">Les métadonnées peuvent être copiées sur disque, sur bande ou sur tout autre dispositif de stockage de masse.</span><span class="sxs-lookup"><span data-stu-id="6d76d-107">Metadata can be copied to disk, tape, or any other mass storage device.</span></span> <span data-ttu-id="6d76d-108">Il doit toujours être enregistré sur le support de sauvegarde au cours d’une opération de sauvegarde et doit être récupéré à partir de ce média au cours d’une opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="6d76d-108">It should always be saved to the backup media during a backup operation, and will need to be retrieved from that media in the course of a restore operation.</span></span>

<span data-ttu-id="6d76d-109">**Attention :** Les détails spécifiques au format et au schéma sont destinés uniquement à une utilisation système.</span><span class="sxs-lookup"><span data-stu-id="6d76d-109">**Caution:** The specific details of the format and schema are for system use only.</span></span> <span data-ttu-id="6d76d-110">Les développeurs ne doivent pas tenter de modifier ou d’utiliser directement la représentation XML des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="6d76d-110">Developers should not attempt to modify or directly use the XML representation of the metadata.</span></span>

<span data-ttu-id="6d76d-111">Les enregistreurs et les demandeurs sont fournis avec diverses méthodes de requête et de définition pour accéder et modifier les composants de sauvegarde et les documents de métadonnées d’écriture :</span><span class="sxs-lookup"><span data-stu-id="6d76d-111">Writers and requesters are provided with a variety of query and set methods to access and modify the Backup Components and Writer Metadata documents:</span></span>

-   [<span data-ttu-id="6d76d-112">Utilisation du document de métadonnées de l’enregistreur</span><span class="sxs-lookup"><span data-stu-id="6d76d-112">Working with the Writer Metadata Document</span></span>](working-with-the-writer-metadata-document.md)
-   [<span data-ttu-id="6d76d-113">Utilisation du document sur les composants de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="6d76d-113">Working with the Backup Components Document</span></span>](working-with-the-backup-components-document.md)
-   [<span data-ttu-id="6d76d-114">Composants de métadonnées VSS</span><span class="sxs-lookup"><span data-stu-id="6d76d-114">VSS Metadata Components</span></span>](vss-metadata-components.md)

 

 



