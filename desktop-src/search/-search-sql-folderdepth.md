---
description: Les prédicats de profondeur de dossier contrôlent l’étendue d’une recherche en spécifiant un chemin d’accès et s’il faut effectuer une traversée profonde ou superficielle.
ms.assetid: 8eadbd42-3538-412e-9bf8-b2355d23437e
title: Prédicats d’étendue et de répertoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2418b2149a5bf05bd000460c787b7f967856c5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112431"
---
# <a name="scope-and-directory-predicates"></a><span data-ttu-id="3a7f6-103">Prédicats d’étendue et de répertoire</span><span class="sxs-lookup"><span data-stu-id="3a7f6-103">SCOPE and DIRECTORY Predicates</span></span>

<span data-ttu-id="3a7f6-104">Les prédicats de profondeur de dossier contrôlent l’étendue d’une recherche en spécifiant un chemin d’accès et s’il faut effectuer une traversée profonde ou superficielle.</span><span class="sxs-lookup"><span data-stu-id="3a7f6-104">Folder depth predicates control the scope of a search by specifying a path and whether to perform a deep or shallow traversal.</span></span> <span data-ttu-id="3a7f6-105">L’exemple suivant illustre la syntaxe des prédicats de profondeur de dossier :</span><span class="sxs-lookup"><span data-stu-id="3a7f6-105">The following shows the syntax of the folder depth predicates:</span></span>


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



<span data-ttu-id="3a7f6-106">Le prédicat est suivi d’un signe égal.</span><span class="sxs-lookup"><span data-stu-id="3a7f6-106">The predicate is followed by an equal sign.</span></span> <span data-ttu-id="3a7f6-107">Le chemin d’accès est indiqué entre guillemets simples et doit commencer par un protocole et un signe deux-points (par exemple,, `file:` `mapi:` ou `csc:` ).</span><span class="sxs-lookup"><span data-stu-id="3a7f6-107">The path is exclosed in single quotes and must begin with a protocol and a colon (for example, `file:`, `mapi:`, or `csc:`).</span></span> <span data-ttu-id="3a7f6-108">Le prédicat SCOPE effectue une traversée profonde du chemin d’accès, y compris tous les sous-dossiers, tandis que le prédicat de répertoire effectue un parcours superficiel uniquement du dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="3a7f6-108">The SCOPE predicate performs a deep traversal of the path, including all subfolders, while the DIRECTORY predicate does a shallow traversal of only the folder specified.</span></span> <span data-ttu-id="3a7f6-109">À l’instar des autres restrictions de langage SQL (SQL), vous pouvez spécifier plusieurs restrictions de profondeur de dossier dans une seule requête.</span><span class="sxs-lookup"><span data-stu-id="3a7f6-109">Like other Structured Query Language (SQL) restrictions, you can specify more than one folder depth restriction in a single query.</span></span>

<span data-ttu-id="3a7f6-110">Pour interroger le catalogue local d’un ordinateur distant, incluez le nom de l’ordinateur avant le catalogue et un chemin d’accès UNC (Universal Naming Convention) sur l’ordinateur distant dans la clause SCOPE ou DIRECTORY.</span><span class="sxs-lookup"><span data-stu-id="3a7f6-110">To query the local catalog of a remote computer, include the computer name before the catalog and a Universal Naming Convention (UNC) path on the remote computer in the SCOPE or DIRECTORY clause.</span></span>

## <a name="examples"></a><span data-ttu-id="3a7f6-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="3a7f6-111">Examples</span></span>


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



<span data-ttu-id="3a7f6-112">L’exemple First SCOPE recherche le \\ \\ dossier de rapports C : Files et tous ses sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="3a7f6-112">The first SCOPE example searches the C:\\Files\\Reports folder and all its subfolders.</span></span> <span data-ttu-id="3a7f6-113">L’exemple de répertoire recherche uniquement dans le dossier racine les rapports C : \\ Files \\ .</span><span class="sxs-lookup"><span data-stu-id="3a7f6-113">The DIRECTORY example searches only the root folder C:\\Files\\Reports.</span></span>

> [!Note]  
> <span data-ttu-id="3a7f6-114">Les barres obliques inverses du système de fichiers ( \\ ) deviennent une barre oblique de style URL (parfois appelée barres obliques) (/).</span><span class="sxs-lookup"><span data-stu-id="3a7f6-114">The file system backslashes (\\) become a URL-style slash marks (sometimes called forward slashes) (/).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3a7f6-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a7f6-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3a7f6-116">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="3a7f6-116">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3a7f6-117">FROM, clause</span><span class="sxs-lookup"><span data-stu-id="3a7f6-117">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="3a7f6-118">Clause WHERE</span><span class="sxs-lookup"><span data-stu-id="3a7f6-118">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



