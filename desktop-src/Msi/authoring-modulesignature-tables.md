---
description: La table ModuleSignature contient toutes les informations nécessaires pour identifier le module de fusion.
ms.assetid: 5f0b4590-dac3-4528-b714-ff760ae8d123
title: Création de tables ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796775b0237c17db4fa21075a792c372bed3e97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518651"
---
# <a name="authoring-modulesignature-tables"></a><span data-ttu-id="48ef6-103">Création de tables ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="48ef6-103">Authoring ModuleSignature Tables</span></span>

<span data-ttu-id="48ef6-104">La [table ModuleSignature](modulesignature-table.md) contient toutes les informations nécessaires pour identifier le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="48ef6-104">The [ModuleSignature table](modulesignature-table.md) contains all the information needed to identify the merge module.</span></span>

<span data-ttu-id="48ef6-105">Le champ ModuleID est la clé primaire de cette table et doit respecter la convention décrite dans [nommage des clés primaires dans les bases de données de module de fusion](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="48ef6-105">The ModuleID field is the primary key for this table and must follow the convention described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span> <span data-ttu-id="48ef6-106">Par exemple, si le nom lisible du module de fusion est MyLibrary et que le GUID du module de fusion est {880DE2F0-CDD8-11D1-A849-006097ABDE17}, l’entrée dans la colonne ModuleID de la table ModuleSignature devient MyLibrary. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.</span><span class="sxs-lookup"><span data-stu-id="48ef6-106">For example, if the readable name of the merge module is MyLibrary and the GUID for the merge module is {880DE2F0-CDD8-11D1-A849-006097ABDE17}, the entry in the ModuleID column of the ModuleSignature table becomes MyLibrary.880DE2F0\_CDD8\_11D1\_A849\_006097ABDE17.</span></span>

<span data-ttu-id="48ef6-107">Entrez l’identificateur décimal pour la langue par défaut du module de fusion dans le champ Language de la table ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="48ef6-107">Enter the decimal identifier for the default language of the merge module into the Language field of the ModuleSignature table.</span></span>

<span data-ttu-id="48ef6-108">Entrez la version du module de fusion dans le champ version.</span><span class="sxs-lookup"><span data-stu-id="48ef6-108">Enter the version of the merge module into the Version field.</span></span>

 

 



