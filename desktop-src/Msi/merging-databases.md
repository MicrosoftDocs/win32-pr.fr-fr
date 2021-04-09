---
description: Vous pouvez utiliser le programme d’installation pour ajouter les informations d’une base de données dans une autre base de données en effectuant une fusion.
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: Fusion de bases de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212355f37a12aa3b92bc10e6e3e41abdcf361dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952593"
---
# <a name="merging-databases"></a><span data-ttu-id="c4ada-103">Fusion de bases de données</span><span class="sxs-lookup"><span data-stu-id="c4ada-103">Merging Databases</span></span>

<span data-ttu-id="c4ada-104">Vous pouvez utiliser le programme d’installation pour ajouter les informations d’une base de données dans une autre base de données en effectuant une fusion.</span><span class="sxs-lookup"><span data-stu-id="c4ada-104">You can use the installer to add the information in one database into another database by performing a merge.</span></span> <span data-ttu-id="c4ada-105">Les [fusions et les transformations](merges-and-transforms.md) opèrent sur une base de données entière, et une fusion combine deux bases de données en une seule.</span><span class="sxs-lookup"><span data-stu-id="c4ada-105">[Merges and Transforms](merges-and-transforms.md) operate on an entire database, and a merge combines two databases into one.</span></span> <span data-ttu-id="c4ada-106">Les fusions sont utiles pour les équipes de développement, car elles permettent de diviser la base de données d’installation d’une application de grande taille en plus petites parties, puis de les recombiner ultérieurement dans la base de données d’installation complète.</span><span class="sxs-lookup"><span data-stu-id="c4ada-106">Merges are useful to development teams because they allow the installation database of large application to be divided into smaller parts and then recombined into the complete installation database later.</span></span>

<span data-ttu-id="c4ada-107">**Pour fusionner plusieurs bases de données de composants dans une seule base de données complète**</span><span class="sxs-lookup"><span data-stu-id="c4ada-107">**To merge several component databases into a single complete database**</span></span>

1.  <span data-ttu-id="c4ada-108">Développez les bases de données de composants partielles séparément.</span><span class="sxs-lookup"><span data-stu-id="c4ada-108">Develop the partial component databases separately.</span></span>
2.  <span data-ttu-id="c4ada-109">Fusionnez chaque base de données de composant dans la base de données principale du produit en appelant la fonction [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) .</span><span class="sxs-lookup"><span data-stu-id="c4ada-109">Merge each component database into the main product database by calling the [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) function.</span></span>

 

 



