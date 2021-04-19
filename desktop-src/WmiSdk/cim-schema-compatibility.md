---
description: Compatibilité du schéma CIM
ms.assetid: 3738914d-dd33-4999-b37f-b4bb94689cd4
ms.tgt_platform: multiple
title: Compatibilité du schéma CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df559469ef6a8284b51951dc365bad6c302ca865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523360"
---
# <a name="cim-schema-compatibility"></a><span data-ttu-id="1ff4a-103">Compatibilité du schéma CIM</span><span class="sxs-lookup"><span data-stu-id="1ff4a-103">CIM Schema Compatibility</span></span>

<span data-ttu-id="1ff4a-104">Un composant clé de l’infrastructure Windows Management Instrumentation (WMI) est un modèle orienté objet des entités gérables dans un système.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-104">A key component of the Windows Management Instrumentation (WMI) infrastructure is an object-oriented model of the manageable entities in a system.</span></span> <span data-ttu-id="1ff4a-105">Le modèle est conforme à un standard géré par la[DMTF](https://www.dmtf.org/standards/wsman)(Desktop Management Task Force) et est connu comme le Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="1ff4a-105">The model conforms to a standard maintained by the Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) and is known as the Common Information Model (CIM).</span></span> <span data-ttu-id="1ff4a-106">Le schéma CIM fournit un mécanisme de description de données unique pour toutes les données qu’ils fournissent.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-106">The CIM schema provides a single data description mechanism for any data that they provide.</span></span>

<span data-ttu-id="1ff4a-107">À compter de Windows 7, WMI est compatible avec la version de schéma CIM 2.17.1 ( [https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171) ).</span><span class="sxs-lookup"><span data-stu-id="1ff4a-107">Starting in Windows 7, WMI is compatible with the CIM Schema version 2.17.1 ([https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171)).</span></span> <span data-ttu-id="1ff4a-108">Les utilisateurs peuvent maintenant compiler un schéma DMTF défini sur un ordinateur Windows.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-108">Users can now compile a DMTF defined schema on a Windows computer.</span></span>

## <a name="benefits-of-cim-schema-version-2171-compatibility"></a><span data-ttu-id="1ff4a-109">Avantages de la compatibilité de la version de schéma CIM 2.17.1</span><span class="sxs-lookup"><span data-stu-id="1ff4a-109">Benefits of CIM Schema version 2.17.1 compatibility</span></span>

-   <span data-ttu-id="1ff4a-110">Lorsqu’un utilisateur télécharge des fichiers de schéma CIM version 2.17.1 ou DMTF, ceux-ci peuvent être compilés correctement sur l’ordinateur Windows cible.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-110">When a user downloads CIM Schema version 2.17.1 or DMTF MOF files, they can be successfully compiled on the target Windows computer.</span></span>
-   <span data-ttu-id="1ff4a-111">La version de schéma CIM 2.17.1 a ajouté la prise en charge du BIOS, des imprimantes, des messages standard, de l’état du système d’exploitation, des paradigmes de gestion de l’alimentation modernes, de la virtualisation et de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-111">The CIM Schema version 2.17.1 added support for BIOS, printers, standard messages, operating system state, modern power management paradigms, virtualization and security.</span></span>
-   <span data-ttu-id="1ff4a-112">La version de schéma CIM 2.1.7.1 offre une prise en charge de profil supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="1ff4a-112">CIM Schema version 2.1.7.1 offers additional profile support.</span></span> <span data-ttu-id="1ff4a-113">Pour plus d’informations, consultez [Cross namespace Association Traversal](cross-namespace-association-traversal.md)</span><span class="sxs-lookup"><span data-stu-id="1ff4a-113">For more information, see [Cross Namespace Association Traversal](cross-namespace-association-traversal.md)</span></span>

 

 



