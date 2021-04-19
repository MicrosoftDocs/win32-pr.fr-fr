---
description: La \_ table ForceCodepage est une table spéciale utilisée pour modifier la page de codes d’un package d’installation. Vous pouvez déterminer ou définir la page de codes en exportant ou en important un fichier d’archive de texte nommé \_ ForceCodepage. IDT.
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132843fa092409b26811afd6a4c1f3e7cf0544f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519663"
---
# <a name="_forcecodepage"></a><span data-ttu-id="47c07-104">\_ForceCodepage</span><span class="sxs-lookup"><span data-stu-id="47c07-104">\_ForceCodepage</span></span>

<span data-ttu-id="47c07-105">La \_ table ForceCodepage est une table spéciale utilisée pour modifier la page de codes d’un package d’installation.</span><span class="sxs-lookup"><span data-stu-id="47c07-105">The \_ForceCodepage table is a special table used for changing the code page of an installation package.</span></span> <span data-ttu-id="47c07-106">Vous pouvez déterminer ou définir la page de codes en exportant ou en important un [fichier d’archive de texte](text-archive-files.md) nommé \_ ForceCodepage. IDT.</span><span class="sxs-lookup"><span data-stu-id="47c07-106">You can determine or set the code page by exporting or importing a [text archive file](text-archive-files.md) named \_ForceCodepage.idt.</span></span>

<span data-ttu-id="47c07-107">Le format de la \_ table ForceCodepage est 2 lignes vides suivies d’une troisième ligne indiquant la page de codes numérique.</span><span class="sxs-lookup"><span data-stu-id="47c07-107">The format of the \_ForceCodepage table is 2 blank lines followed by a third line that indicates the numeric code page.</span></span> <span data-ttu-id="47c07-108">Par exemple, un \_ fichier ForceCodepage table. IDT pour une base de données japonaise se présenterait comme suit.</span><span class="sxs-lookup"><span data-stu-id="47c07-108">For example, a \_ForceCodepage table .idt file for a Japanese database would look as follows.</span></span> <span data-ttu-id="47c07-109">Dans ce cas, la page de codes numérique est 932.</span><span class="sxs-lookup"><span data-stu-id="47c07-109">The numeric code page in this case is 932.</span></span>

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

<span data-ttu-id="47c07-110">Pour plus d’informations sur l’utilisation de \_ ForceCodepage pour obtenir ou définir la page de codes d’une base de données, consultez les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="47c07-110">For more information on how to use \_ForceCodepage to get or set the code page of a database see the following topics.</span></span>

-   [<span data-ttu-id="47c07-111">Gestion des pages de codes (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="47c07-111">Code Page Handling (Windows Installer)</span></span>](code-page-handling-windows-installer-.md)
-   [<span data-ttu-id="47c07-112">Détermination de la page de codes d’une base de données d’installation</span><span class="sxs-lookup"><span data-stu-id="47c07-112">Determining an Installation Database's Code Page</span></span>](determining-an-installation-database-s-code-page.md)
-   [<span data-ttu-id="47c07-113">Définition de la page de codes d’une base de données</span><span class="sxs-lookup"><span data-stu-id="47c07-113">Setting the Code Page of a Database</span></span>](setting-the-code-page-of-a-database.md)

<span data-ttu-id="47c07-114">La \_ table ForceCodepage est une pseudo-table spéciale utilisée pour modifier la page de codes d’un package d’installation.</span><span class="sxs-lookup"><span data-stu-id="47c07-114">The \_ForceCodepage table is a special pseudo table used for changing the code page of an installation package.</span></span> <span data-ttu-id="47c07-115">L’utilisation de la \_ table ForceCodepage définit de manière inconditionnelle la base de données sur la page de codes sans effectuer de validation pour déterminer si les données présentes dans la base de données peuvent être traduites dans la nouvelle page de codes.</span><span class="sxs-lookup"><span data-stu-id="47c07-115">Using the \_ForceCodepage table unconditionally sets the database to the code page without performing any validation as to whether the data currently in the database can be translated to the new code page.</span></span> <span data-ttu-id="47c07-116">Il est toujours recommandé de modifier la page de codes d’une base de données à partir d’une base de données indépendante de la langue.</span><span class="sxs-lookup"><span data-stu-id="47c07-116">It is always recommended that changing the code page of a database start with a language neutral database.</span></span>

 

 



