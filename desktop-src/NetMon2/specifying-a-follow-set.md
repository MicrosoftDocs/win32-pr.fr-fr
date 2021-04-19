---
description: Un jeu suivant spécifie les protocoles qui suivent un protocole. Moniteur réseau utilise un jeu de suivi lorsque l’analyseur ne parvient pas à identifier le protocole suivant à partir des données dans une instance de protocole.
ms.assetid: 9e73c724-a540-42f8-b273-4f02c39d81c4
title: Spécification d’un jeu de suivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9e36268be82d2fed7c3d0c56a078e41dff1733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516497"
---
# <a name="specifying-a-follow-set"></a><span data-ttu-id="51e33-104">Spécification d’un jeu de suivi</span><span class="sxs-lookup"><span data-stu-id="51e33-104">Specifying a Follow Set</span></span>

<span data-ttu-id="51e33-105">Un jeu suivant spécifie les protocoles qui suivent un protocole.</span><span class="sxs-lookup"><span data-stu-id="51e33-105">A follow set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="51e33-106">Moniteur réseau utilise un jeu de suivi lorsque l’analyseur ne parvient pas à identifier le protocole suivant à partir des données dans une instance de protocole.</span><span class="sxs-lookup"><span data-stu-id="51e33-106">Network Monitor uses a follow set when the parser cannot identify the next protocol from the data in a protocol instance.</span></span>

<span data-ttu-id="51e33-107">Par exemple, l’analyseur NetBIOS spécifie un jeu de suivi, car les données du protocole NetBIOS n’identifient pas le protocole suivant.</span><span class="sxs-lookup"><span data-stu-id="51e33-107">For example, the NetBIOS parser specifies a follow set because the data in the NetBIOS protocol does not identify which protocol is next.</span></span> <span data-ttu-id="51e33-108">Par conséquent, l’analyseur NetBIOS doit créer un ensemble de tous les protocoles qui peuvent être suivis.</span><span class="sxs-lookup"><span data-stu-id="51e33-108">As a result the NetBIOS parser must create a follow set of all the protocols that may follow.</span></span>

<span data-ttu-id="51e33-109">L’exemple de code suivant identifie le jeu de suivi NetBIOS dans le fichier [*Parser.ini*](p.md) .</span><span class="sxs-lookup"><span data-stu-id="51e33-109">The following code example identifies the NetBIOS follow set in the [*Parser.ini*](p.md) file.</span></span> <span data-ttu-id="51e33-110">Le jeu suivant contient les protocoles SMB (Server Message Block) et MSRPC (Microsoft Remote Procedure Call).</span><span class="sxs-lookup"><span data-stu-id="51e33-110">The follow set contains server message block (SMB), and Microsoft remote procedure call (MSRPC) protocols.</span></span> <span data-ttu-id="51e33-111">Il s’agit des seuls protocoles qui peuvent suivre une instance du protocole NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="51e33-111">These are the only protocols that can follow an instance of the NetBIOS protocol.</span></span>

``` syntax
[NETBIOS]
   Comment    = "Network Basic Input/Output System protocol"
   FollowSet  = SMB, MSRPC
   HelpFile   =
```

<span data-ttu-id="51e33-112">Un analyseur spécifie un jeu de suivi lors de l’implémentation de la fonction [**ParserAutoInstallInfo**](parserautoinstallinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="51e33-112">A parser specifies a follow set during the implementation of the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) function.</span></span> <span data-ttu-id="51e33-113">Un analyseur peut spécifier quels protocoles précèdent et quels protocoles suivent.</span><span class="sxs-lookup"><span data-stu-id="51e33-113">A parser can specify which protocols precede, and which protocols follow.</span></span> <span data-ttu-id="51e33-114">Lorsqu’un analyseur spécifie les protocoles qui précèdent, Moniteur réseau ajoute le protocole d’analyseur aux ensembles suivants des protocoles spécifiés.</span><span class="sxs-lookup"><span data-stu-id="51e33-114">When a parser specifies the protocols that precede, Network Monitor adds the parser protocol to the follow sets of the specified protocols.</span></span> <span data-ttu-id="51e33-115">Lorsqu’un analyseur spécifie les protocoles qui suivent, Moniteur réseau crée une nouvelle section dans le fichier Parser.ini qui comprend le jeu suivant de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="51e33-115">When a parser specifies the protocols that follow, Network Monitor creates a new section in the Parser.ini file that includes the follow set of the parser.</span></span>

 

 



