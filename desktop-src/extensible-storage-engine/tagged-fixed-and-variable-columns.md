---
description: 'En savoir plus sur : colonnes avec balises, fixes et variables'
title: Colonnes avec balises, fixes et variables
TOCTitle: Tagged, Fixed and Variable Columns
ms:assetid: 78a905b8-71a9-4b2e-b9f2-c81bfe3aef8e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269304(v=EXCHG.10)
ms:contentKeyID: 32765595
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 3f27237c5f75874f7320f675affe20f3833084b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484872"
---
# <a name="tagged-fixed-and-variable-columns"></a><span data-ttu-id="bbaf0-103">Colonnes avec balises, fixes et variables</span><span class="sxs-lookup"><span data-stu-id="bbaf0-103">Tagged, Fixed and Variable Columns</span></span>


<span data-ttu-id="bbaf0-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="bbaf0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="tagged-fixed-and-variable-columns"></a><span data-ttu-id="bbaf0-105">Colonnes avec balises, fixes et variables</span><span class="sxs-lookup"><span data-stu-id="bbaf0-105">Tagged, Fixed and Variable Columns</span></span>

<span data-ttu-id="bbaf0-106">Les colonnes de longueur variable, corrigées et marquées sont les types de colonnes primaires pris en charge par ESE.</span><span class="sxs-lookup"><span data-stu-id="bbaf0-106">Tagged, fixed, and variable-length columns are the primary column types supported by ESE.</span></span> <span data-ttu-id="bbaf0-107">Les colonnes avec balises ne sont pas présentes dans un enregistrement sauf si les données sont stockées dans la colonne et peuvent être fixes ou de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="bbaf0-107">Tagged columns are not present in a record unless data is stored in the column, and may be fixed or variable length.</span></span> <span data-ttu-id="bbaf0-108">Les colonnes avec balises peuvent également contenir plusieurs valeurs dans un seul enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bbaf0-108">Tagged columns can also contain more than one value in a single record.</span></span> <span data-ttu-id="bbaf0-109">Les colonnes fixes prennent la même quantité d’espace dans chaque ligne et requièrent 1 bit pour représenter la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="bbaf0-109">Fixed columns take the same amount of space in every row, and require 1 bit to represent the NULL value.</span></span> <span data-ttu-id="bbaf0-110">Les colonnes de longueur variable requièrent 2 octets pour représenter la taille et la valeur NULL, et occupent une quantité variable d’espace dans chaque enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bbaf0-110">Variable length columns require 2 bytes to represent the size and NULL value, and occupy a variable amount of space in each record.</span></span> <span data-ttu-id="bbaf0-111">Pour plus d’informations sur les colonnes avec balises et fixes, consultez l’option Jet_bitColumnTagged et Jet_bitColumnFixed dans le membre **Grbit** de [JET_COLUMNDEF](./jet-columndef-structure.md) structure utilisée dans l’appel à [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="bbaf0-111">For more information on the tagged and fixed columns, see the Jet_bitColumnTagged, and Jet_bitColumnFixed option in the **grbit** member of [JET_COLUMNDEF](./jet-columndef-structure.md) structure used in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span>

<span data-ttu-id="bbaf0-112">Les colonnes de longueur variable sont déterminées par le type de colonne défini dans le paramètre *coltyp* de l’appel à [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="bbaf0-112">Variable-length columns are determined by the column type that is set in the *coltyp* parameter in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="bbaf0-113">Les types de colonnes suivants peuvent être fixes ou de longueur variable selon que l’option Jet_bitColumnFixed est définie :</span><span class="sxs-lookup"><span data-stu-id="bbaf0-113">The following column types may be fixed or variable length depending on whether the Jet_bitColumnFixed option is set:</span></span>

  - <span data-ttu-id="bbaf0-114">JET_coltypBinary</span><span class="sxs-lookup"><span data-stu-id="bbaf0-114">JET_coltypBinary</span></span>

  - <span data-ttu-id="bbaf0-115">JET_coltypText</span><span class="sxs-lookup"><span data-stu-id="bbaf0-115">JET_coltypText</span></span>

  - <span data-ttu-id="bbaf0-116">JET_coltypLongBinary</span><span class="sxs-lookup"><span data-stu-id="bbaf0-116">JET_coltypLongBinary</span></span>

  - <span data-ttu-id="bbaf0-117">JET_coltypLongText</span><span class="sxs-lookup"><span data-stu-id="bbaf0-117">JET_coltypLongText</span></span>

<span data-ttu-id="bbaf0-118">En général, les données de l’enregistrement sont stockées avec la plage fixe en premier, la plage de variables suivante et la plage marquée stockée en dernier.</span><span class="sxs-lookup"><span data-stu-id="bbaf0-118">In general, data in the record is stored with the fixed range first, the variable range next, and the tagged range stored last.</span></span> <span data-ttu-id="bbaf0-119">Le diagramme suivant montre comment les enregistrements sont stockés dans la table.</span><span class="sxs-lookup"><span data-stu-id="bbaf0-119">The following diagram shows how the records are stored in the table.</span></span> <span data-ttu-id="bbaf0-120">Comme indiqué dans le diagramme, la plage avec balises peut contenir des colonnes avec plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="bbaf0-120">As shown in the diagram, the tagged range may contain columns with multiple values.</span></span>

<span data-ttu-id="bbaf0-121">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span><span class="sxs-lookup"><span data-stu-id="bbaf0-121">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span></span>
