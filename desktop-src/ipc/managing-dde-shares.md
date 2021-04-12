---
description: L’échange de données réseau fournit des fonctions qui vous permettent de supprimer un partage, d’obtenir ou de définir des informations de partage ou d’énumérer des partages.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Gestion des partages DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcc8c7d2eb3983aaabd054b9b729daea176bb10
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104321357"
---
# <a name="managing-dde-shares"></a><span data-ttu-id="5b689-103">Gestion des partages DDE</span><span class="sxs-lookup"><span data-stu-id="5b689-103">Managing DDE Shares</span></span>

<span data-ttu-id="5b689-104">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5b689-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="5b689-105">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="5b689-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="5b689-106">L’échange de données réseau fournit des fonctions qui vous permettent de supprimer un partage, d’obtenir ou de définir des informations de partage ou d’énumérer des partages.</span><span class="sxs-lookup"><span data-stu-id="5b689-106">Network DDE provides functions that allow you to delete a share, get or set share information, or enumerate shares.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b689-107">Tâche</span><span class="sxs-lookup"><span data-stu-id="5b689-107">Task</span></span></th>
<th><span data-ttu-id="5b689-108">Procédure</span><span class="sxs-lookup"><span data-stu-id="5b689-108">Procedure</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b689-109">Supprimer un partage DDE</span><span class="sxs-lookup"><span data-stu-id="5b689-109">Delete a DDE share</span></span></td>
<td><span data-ttu-id="5b689-110">Utilisez la fonction <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5b689-110">Use the <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b689-111">Recevoir des informations sur le partage DDE</span><span class="sxs-lookup"><span data-stu-id="5b689-111">Get DDE share information</span></span></td>
<td><span data-ttu-id="5b689-112">Utilisez la fonction <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5b689-112">Use the <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> function.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b689-113">Définir les informations de partage DDE</span><span class="sxs-lookup"><span data-stu-id="5b689-113">Set DDE share information</span></span></td>
<td><span data-ttu-id="5b689-114">Utilisez la fonction <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5b689-114">Use the <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b689-115">Énumérer les partages DDE</span><span class="sxs-lookup"><span data-stu-id="5b689-115">Enumerate DDE shares</span></span></td>
<td><span data-ttu-id="5b689-116">Utilisez la fonction <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5b689-116">Use the <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> function.</span></span> <span data-ttu-id="5b689-117">Vous pouvez également énumérer les partages DDE approuvés à l’aide de la fonction <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5b689-117">You can also enumerate the trusted DDE shares by using the <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b689-118">Énumérer les utilisateurs connectés</span><span class="sxs-lookup"><span data-stu-id="5b689-118">Enumerate connected users</span></span></td>
<td><span data-ttu-id="5b689-119">Utilisez la fonction <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5b689-119">Use the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b689-120">Modifier le nom de partage DDE</span><span class="sxs-lookup"><span data-stu-id="5b689-120">Change the DDE share name</span></span></td>
<td><span data-ttu-id="5b689-121">Supprimez l’ancien partage et créez un nouveau partage.</span><span class="sxs-lookup"><span data-stu-id="5b689-121">Delete the old share and create a new share.</span></span>
<ol>
<li><span data-ttu-id="5b689-122">Récupérez les informations de partage à l’aide de <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5b689-122">Retrieve the share information using <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span></span></li>
<li><span data-ttu-id="5b689-123">Supprimez le partage à l’aide de <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5b689-123">Remove the share using <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>.</span></span></li>
<li><span data-ttu-id="5b689-124">Modifiez le membre <strong>lpszShareName</strong> de la structure <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> retournée par <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5b689-124">Change the <strong>lpszShareName</strong> member of the <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> structure returned by <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span></span></li>
<li><span data-ttu-id="5b689-125">Transmettez la structure <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> modifiée à <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5b689-125">Pass the modified <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> structure to <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

