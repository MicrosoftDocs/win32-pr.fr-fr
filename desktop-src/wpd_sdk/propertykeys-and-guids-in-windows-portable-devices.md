---
description: PROPERTYKEYs et GUID dans les appareils mobiles Windows
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: PROPERTYKEYs et GUID dans les appareils mobiles Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28cbe76b76eda04852cd1afcbb11b85b0a185d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866506"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a><span data-ttu-id="8c7bb-103">PROPERTYKEYs et GUID dans les appareils mobiles Windows</span><span class="sxs-lookup"><span data-stu-id="8c7bb-103">PROPERTYKEYs and GUIDs in Windows Portable Devices</span></span>

<span data-ttu-id="8c7bb-104">Une propriété ou une commande est identifiée par une structure PROPERTYKEY.</span><span class="sxs-lookup"><span data-stu-id="8c7bb-104">A property or command is identified by a PROPERTYKEY structure.</span></span> <span data-ttu-id="8c7bb-105">Une structure PROPERTYKEY est constituée de deux parties : un GUID (le membre fmtid) et un DWORD (le membre PID).</span><span class="sxs-lookup"><span data-stu-id="8c7bb-105">A PROPERTYKEY structure is made up of two parts: a GUID (the fmtid member) and a DWORD (the pid member).</span></span> <span data-ttu-id="8c7bb-106">La partie GUID est utilisée pour indiquer la catégorie à laquelle appartient la propriété ou la commande (autrement dit, les propriétés associées appartiennent à la même catégorie et les commandes associées appartiennent à la même catégorie ; elles ont donc le même fmtid).</span><span class="sxs-lookup"><span data-stu-id="8c7bb-106">The GUID part is used to indicate the category the property or command belongs to (that is, related properties belong to the same category and related commands belong to the same category; therefore they will have the same fmtid).</span></span> <span data-ttu-id="8c7bb-107">La partie DWORD indique la propriété ou l’ID de commande et est utilisée pour distinguer les propriétés ou les commandes individuelles au sein d’une catégorie de propriété ou de commande (autrement dit, les valeurs PID pour les propriétés ou les commandes dans la même catégorie seront différentes).</span><span class="sxs-lookup"><span data-stu-id="8c7bb-107">The DWORD part indicates the property or command ID, and is used to distinguish the individual properties or commands within a property or command category (that is, the pid values for properties or commands in the same category will be different).</span></span>

<span data-ttu-id="8c7bb-108">La section Références de ce document décrit toutes les valeurs de PROPERTYKEY définies par WPD. ces valeurs correspondent à des commandes, des propriétés et des ressources.</span><span class="sxs-lookup"><span data-stu-id="8c7bb-108">The reference section of this document describes all the PROPERTYKEY values defined by WPD; these values correspond to commands, properties, and resources.</span></span> <span data-ttu-id="8c7bb-109">Si vous créez une valeur PROPERTYKEY personnalisée, vous devez définir une nouvelle catégorie **GUID** ; ne réutilisez pas les valeurs de **GUID** wpd ou risquez d’être en conflit avec les valeurs PROPERTYKEYs existantes et futures spécifiées dans wpd.</span><span class="sxs-lookup"><span data-stu-id="8c7bb-109">If you create a custom PROPERTYKEY value, you should define a new **GUID** category; do not reuse the WPD **GUID** values or you risk conflicting with existing and future WPD-specified PROPERTYKEYs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c7bb-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c7bb-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c7bb-111">**Vue d’ensemble de l’application**</span><span class="sxs-lookup"><span data-stu-id="8c7bb-111">**Application Overview**</span></span>](application-overview.md)
</dt> <dt>

[<span data-ttu-id="8c7bb-112">**Commandes**</span><span class="sxs-lookup"><span data-stu-id="8c7bb-112">**Commands**</span></span>](commands.md)
</dt> <dt>

[<span data-ttu-id="8c7bb-113">**GUID de format d’objet**</span><span class="sxs-lookup"><span data-stu-id="8c7bb-113">**Object Format GUIDs**</span></span>](object-format-guids.md)
</dt> <dt>

[<span data-ttu-id="8c7bb-114">**Propriétés et attributs**</span><span class="sxs-lookup"><span data-stu-id="8c7bb-114">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> <dt>

[<span data-ttu-id="8c7bb-115">**Conditions requises pour les objets**</span><span class="sxs-lookup"><span data-stu-id="8c7bb-115">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



