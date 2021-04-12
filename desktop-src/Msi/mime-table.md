---
description: La table MIME associe un type de contenu MIME à une extension de nom de fichier ou un CLSID pour générer l’extension ou les informations de serveur COM requises pour la publication du contenu MIME (Multipurpose Internet Mail Extensions).
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: Table MIME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca11c8596e8f3735872c88668211953fc2b18b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204184"
---
# <a name="mime-table"></a><span data-ttu-id="13de5-103">Table MIME</span><span class="sxs-lookup"><span data-stu-id="13de5-103">MIME Table</span></span>

<span data-ttu-id="13de5-104">La table MIME associe un type de contenu MIME à une extension de nom de fichier ou un CLSID pour générer l’extension ou les informations de serveur COM requises pour la publication du contenu MIME (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="13de5-104">The MIME table associates a MIME content type with a file name extension or a CLSID to generate the extension or COM server information required for advertisement of the MIME (Multipurpose Internet Mail Extensions) content.</span></span>

<span data-ttu-id="13de5-105">La table MIME contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="13de5-105">The MIME table has the following columns.</span></span>



| <span data-ttu-id="13de5-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="13de5-106">Column</span></span>      | <span data-ttu-id="13de5-107">Type</span><span class="sxs-lookup"><span data-stu-id="13de5-107">Type</span></span>             | <span data-ttu-id="13de5-108">Clé</span><span class="sxs-lookup"><span data-stu-id="13de5-108">Key</span></span> | <span data-ttu-id="13de5-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="13de5-109">Nullable</span></span> |
|-------------|------------------|-----|----------|
| <span data-ttu-id="13de5-110">ContentType</span><span class="sxs-lookup"><span data-stu-id="13de5-110">ContentType</span></span> | [<span data-ttu-id="13de5-111">Text</span><span class="sxs-lookup"><span data-stu-id="13de5-111">Text</span></span>](text.md) | <span data-ttu-id="13de5-112">O</span><span class="sxs-lookup"><span data-stu-id="13de5-112">Y</span></span>   | <span data-ttu-id="13de5-113">N</span><span class="sxs-lookup"><span data-stu-id="13de5-113">N</span></span>        |
| <span data-ttu-id="13de5-114">Extension\_</span><span class="sxs-lookup"><span data-stu-id="13de5-114">Extension\_</span></span> | [<span data-ttu-id="13de5-115">Text</span><span class="sxs-lookup"><span data-stu-id="13de5-115">Text</span></span>](text.md) | <span data-ttu-id="13de5-116">N</span><span class="sxs-lookup"><span data-stu-id="13de5-116">N</span></span>   | <span data-ttu-id="13de5-117">N</span><span class="sxs-lookup"><span data-stu-id="13de5-117">N</span></span>        |
| <span data-ttu-id="13de5-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="13de5-118">CLSID</span></span>       | [<span data-ttu-id="13de5-119">GUID</span><span class="sxs-lookup"><span data-stu-id="13de5-119">GUID</span></span>](guid.md) | <span data-ttu-id="13de5-120">N</span><span class="sxs-lookup"><span data-stu-id="13de5-120">N</span></span>   | <span data-ttu-id="13de5-121">O</span><span class="sxs-lookup"><span data-stu-id="13de5-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="13de5-122">Colonnes</span><span class="sxs-lookup"><span data-stu-id="13de5-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="13de5-123"><span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>Indiquez</span><span class="sxs-lookup"><span data-stu-id="13de5-123"><span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType</span></span>
</dt> <dd>

<span data-ttu-id="13de5-124">Cette colonne est un identificateur pour le contenu MIME.</span><span class="sxs-lookup"><span data-stu-id="13de5-124">This column is an identifier for the MIME content.</span></span> <span data-ttu-id="13de5-125">Il est généralement écrit sous la forme d’un type/format.</span><span class="sxs-lookup"><span data-stu-id="13de5-125">It is commonly written in the form of type/format.</span></span>

</dd> <dt>

<span data-ttu-id="13de5-126"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Poste\_</span><span class="sxs-lookup"><span data-stu-id="13de5-126"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_</span></span>
</dt> <dd>

<span data-ttu-id="13de5-127">Cette colonne contient l’extension de serveur qui doit être associée au contenu MIME, sans le point.</span><span class="sxs-lookup"><span data-stu-id="13de5-127">This column contains the server extension that is to be associated with the MIME content, without the dot.</span></span> <span data-ttu-id="13de5-128">Cette colonne est une clé étrangère dans la [table d’extension](extension-table.md).</span><span class="sxs-lookup"><span data-stu-id="13de5-128">This column is a foreign key into the [Extension table](extension-table.md).</span></span> <span data-ttu-id="13de5-129">La table d’extension contient des informations sur le serveur d’extension de nom de fichier utilisées dans le cadre de la publication.</span><span class="sxs-lookup"><span data-stu-id="13de5-129">The Extension table contains file name extension server information which is used as a part of advertisement.</span></span>

</dd> <dt>

<span data-ttu-id="13de5-130"><span id="CLSID"></span><span id="clsid"></span>IDENTIFICATEUR</span><span class="sxs-lookup"><span data-stu-id="13de5-130"><span id="CLSID"></span><span id="clsid"></span>CLSID</span></span>
</dt> <dd>

<span data-ttu-id="13de5-131">Cette colonne contient le CLSID du serveur COM qui doit être associé au contenu MIME.</span><span class="sxs-lookup"><span data-stu-id="13de5-131">This column contains the COM server CLSID that is to be associated with the MIME content.</span></span> <span data-ttu-id="13de5-132">Le CLSID de cette colonne peut être une clé étrangère dans la [table de classe](class-table.md) ou il peut s’agir d’un CLSID qui existe déjà sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="13de5-132">The CLSID in this column can be a foreign key into the [Class table](class-table.md) or it can be a CLSID that already exists on the user's machine.</span></span> <span data-ttu-id="13de5-133">La table de classe contient des informations relatives au serveur COM, qui sont utilisées dans le cadre de la publication.</span><span class="sxs-lookup"><span data-stu-id="13de5-133">The Class table contains COM server-related information which is used as a part of advertisement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13de5-134">Notes</span><span class="sxs-lookup"><span data-stu-id="13de5-134">Remarks</span></span>

<span data-ttu-id="13de5-135">Cette table est référencée lorsque l' [action RegisterMIMEInfo](registermimeinfo-action.md) ou l' [action UnregisterMIMEInfo](unregistermimeinfo-action.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="13de5-135">This table is referred to when the [RegisterMIMEInfo action](registermimeinfo-action.md) or the [UnregisterMIMEInfo action](unregistermimeinfo-action.md) is executed.</span></span> <span data-ttu-id="13de5-136">En mode publication, l’action RegisterMIMEInfo enregistre toutes les informations MIME pour les serveurs à partir de la table MIME pour laquelle la fonctionnalité correspondante est activée.</span><span class="sxs-lookup"><span data-stu-id="13de5-136">In advertise mode, the RegisterMIMEInfo action registers all MIME information for servers from the MIME table for which the corresponding feature is enabled.</span></span> <span data-ttu-id="13de5-137">Dans le cas contraire, l’action enregistre les informations MIME pour les serveurs de la table MIME pour lesquels la fonctionnalité correspondante est actuellement sélectionnée pour être installée.</span><span class="sxs-lookup"><span data-stu-id="13de5-137">Otherwise the action registers MIME information for servers from the MIME table for which the corresponding feature is currently selected to be installed.</span></span> <span data-ttu-id="13de5-138">L' [action UnregisterMIMEInfo](unregistermimeinfo-action.md) annule l’enregistrement des informations de Registre liées à MIME à partir du système.</span><span class="sxs-lookup"><span data-stu-id="13de5-138">The [UnregisterMIMEInfo action](unregistermimeinfo-action.md) unregisters MIME-related registry information from the system.</span></span> <span data-ttu-id="13de5-139">L’action annule l’enregistrement des informations MIME pour les serveurs de la table MIME pour lesquels la fonctionnalité correspondante est actuellement sélectionnée pour être désinstallée.</span><span class="sxs-lookup"><span data-stu-id="13de5-139">The action unregisters MIME information for servers from the MIME table for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="validation"></a><span data-ttu-id="13de5-140">Validation</span><span class="sxs-lookup"><span data-stu-id="13de5-140">Validation</span></span>

<dl>

[<span data-ttu-id="13de5-141">ICE03</span><span class="sxs-lookup"><span data-stu-id="13de5-141">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="13de5-142">ICE06</span><span class="sxs-lookup"><span data-stu-id="13de5-142">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="13de5-143">ICE15</span><span class="sxs-lookup"><span data-stu-id="13de5-143">ICE15</span></span>](ice15.md)  
[<span data-ttu-id="13de5-144">ICE32</span><span class="sxs-lookup"><span data-stu-id="13de5-144">ICE32</span></span>](ice32.md)  
</dl>

 

 



