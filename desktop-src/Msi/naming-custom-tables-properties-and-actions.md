---
description: Les auteurs de package doivent s’assurer que les noms de toutes les tables, propriétés ou actions personnalisées définies dans leur package n’entrent pas en conflit avec les noms de tables, de propriétés ou d’actions standard qui sont natives au Windows Installer.
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: Attribution d’un nom aux tables, propriétés et actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aabd35fb1456f6aefbd05d486b1d86420bf5013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864082"
---
# <a name="naming-custom-tables-properties-and-actions"></a><span data-ttu-id="d4d6d-103">Attribution d’un nom aux tables, propriétés et actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="d4d6d-103">Naming Custom Tables, Properties, and Actions</span></span>

<span data-ttu-id="d4d6d-104">Les auteurs de package doivent s’assurer que les noms de toutes les tables, propriétés ou actions personnalisées définies dans leur package n’entrent pas en conflit avec les noms de tables, de propriétés ou d’actions standard qui sont natives au Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d4d6d-104">Package authors should ensure that the names of any custom tables, properties, or actions defined in their package will not conflict with the names of standard tables, properties, or actions that are native to the Windows Installer.</span></span>

<span data-ttu-id="d4d6d-105">Les auteurs de packages doivent respecter les instructions suivantes pour les noms de table, de propriété ou d’action personnalisés.</span><span class="sxs-lookup"><span data-stu-id="d4d6d-105">Package authors should adhere to the following guidelines for custom table, property, or action names.</span></span>

-   <span data-ttu-id="d4d6d-106">Créez des noms pour les tables, les propriétés ou les actions personnalisées qui ont un préfixe qui identifie votre application.</span><span class="sxs-lookup"><span data-stu-id="d4d6d-106">Make names for custom tables, properties, or actions that have a prefix that identifies your application.</span></span>
-   <span data-ttu-id="d4d6d-107">N’utilisez jamais de nom avec MSI comme préfixe.</span><span class="sxs-lookup"><span data-stu-id="d4d6d-107">Never use a name with Msi as the prefix.</span></span> <span data-ttu-id="d4d6d-108">À partir de Windows Installer 2,0, toutes les nouvelles propriétés, actions et tables natives Windows Installer reçoivent des noms préfixés par MSI.</span><span class="sxs-lookup"><span data-stu-id="d4d6d-108">Starting with Windows Installer 2.0, all new native Windows Installer properties, actions, and tables are given names prefixed by Msi.</span></span> <span data-ttu-id="d4d6d-109">Ce préfixe ne respecte pas la casse, par exemple MsiNewInternalTable.</span><span class="sxs-lookup"><span data-stu-id="d4d6d-109">This prefix is not case sensitive, for example MsiNewInternalTable.</span></span> <span data-ttu-id="d4d6d-110">Étant donné que le préfixe ne respecte pas la casse, les auteurs doivent éviter tous les cas du préfixe msi.</span><span class="sxs-lookup"><span data-stu-id="d4d6d-110">Because the prefix is not case sensitive, authors should avoid all cases of the Msi prefix.</span></span>

<span data-ttu-id="d4d6d-111">Pour plus d’informations, consultez [noms de tables](table-names.md).</span><span class="sxs-lookup"><span data-stu-id="d4d6d-111">For more information, see [Table Names](table-names.md).</span></span>

 

 



