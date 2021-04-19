---
description: Un jeu de remise spécifie les protocoles qui suivent un protocole. L’analyseur utilise un jeu de remise uniquement lorsque l’analyseur peut identifier le protocole suivant à partir des données dans une instance de protocole.
ms.assetid: d1f44646-98ee-4e3a-a81a-83d6c87c23f4
title: Spécification d’un jeu de remise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9acb421963bea3ffaa70b6165c6ffceee138e38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524485"
---
# <a name="specifying-a-handoff-set"></a><span data-ttu-id="79d23-104">Spécification d’un jeu de remise</span><span class="sxs-lookup"><span data-stu-id="79d23-104">Specifying a Handoff Set</span></span>

<span data-ttu-id="79d23-105">Un jeu de remise spécifie les protocoles qui suivent un protocole.</span><span class="sxs-lookup"><span data-stu-id="79d23-105">A handoff set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="79d23-106">L’analyseur utilise un jeu de remise uniquement lorsque l’analyseur peut identifier le protocole suivant à partir des données dans une instance de protocole.</span><span class="sxs-lookup"><span data-stu-id="79d23-106">The parser uses a handoff set only when the parser can identify the next protocol from the data in a protocol instance.</span></span>

<span data-ttu-id="79d23-107">Par exemple, le protocole TCP a une propriété port qui identifie le protocole qui suit le protocole TCP.</span><span class="sxs-lookup"><span data-stu-id="79d23-107">For example, the TCP protocol has a port property that identifies the protocol that follows the TCP protocol.</span></span> <span data-ttu-id="79d23-108">Une valeur de propriété de 20 indique que le protocole suivant est FTP.</span><span class="sxs-lookup"><span data-stu-id="79d23-108">A property value of 20 indicates that the next protocol is FTP.</span></span> <span data-ttu-id="79d23-109">Une valeur de propriété de 53 indique que le protocole suivant est DNS.</span><span class="sxs-lookup"><span data-stu-id="79d23-109">A property value of 53 indicates that the next protocol is DNS.</span></span> <span data-ttu-id="79d23-110">Étant donné que la propriété port identifie le protocole qui suit, l’analyseur TCP peut utiliser le jeu de remise suivant pour obtenir un descripteur pour le protocole que la propriété Port spécifie.</span><span class="sxs-lookup"><span data-stu-id="79d23-110">Because the port property identifies the protocol that follows, the TCP parser can use the following handoff set to get a handle for the protocol that the port property specifies.</span></span>

``` syntax
[TCP_HandoffSet]
  20    = FTP
  21    = FTP
  23    = TELNET
  25    = SMTP
  53    = DNS
  79    = FINGER
  80    = HTTP
  102   = ISO
  111   = RPC
  119   = NNTP
  137   = NBT, 1000
  138   = NBT, 1002
  139   = NBT, 1001
  389   = LDAP
  445   = NBT, 1001
  515   = LPR
  612   = HMMP
  613   = HMMP
  1024  = NBT, 1001
  1047  = NBT, 1001
  1362  = TDS
  1433  = TDS
  1723  = PPTP
  3020  = NBT, 1001
  3268  = LDAP
  5678  = PPTP
```

<span data-ttu-id="79d23-111">Les jeux de remise sont stockés dans le fichier INI de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="79d23-111">Handoff sets are stored in the parser INI file.</span></span> <span data-ttu-id="79d23-112">Par exemple, le jeu de remise TCP précédent se trouve dans tcpip.ini fichier.</span><span class="sxs-lookup"><span data-stu-id="79d23-112">For example, the preceding TCP handoff set is located in tcpip.ini file.</span></span> <span data-ttu-id="79d23-113">Notez que si une DLL de l’analyseur prend en charge plusieurs protocoles, chaque analyseur qui utilise un jeu de remise a son propre emplacement dans le fichier INI.</span><span class="sxs-lookup"><span data-stu-id="79d23-113">Note that if a parser DLL supports multiple protocols, each parser that uses a handoff set has its own location in the INI file.</span></span>

<span data-ttu-id="79d23-114">Les informations de jeu de remise sont spécifiées lors de l’implémentation de la fonction [**ParserAutoInstallInfo**](parserautoinstallinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="79d23-114">Handoff set information is specified during the implementation of the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) function.</span></span> <span data-ttu-id="79d23-115">L’analyseur peut spécifier les protocoles qui précèdent le protocole de l’analyseur et les protocoles qui suivent le protocole de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="79d23-115">The parser can specify the protocols that precede the parser protocol, and the protocols that follow the parser protocol.</span></span> <span data-ttu-id="79d23-116">Moniteur réseau prend tous les protocoles qui précèdent et ajoute le protocole d’analyse aux sections de l’ensemble suivant du fichier INI de l’analyseur, pour chaque protocole précédent.</span><span class="sxs-lookup"><span data-stu-id="79d23-116">Network Monitor takes all the protocols that precede, and adds the parser protocol to the follow set sections of the parser INI file — for each preceding protocol.</span></span> <span data-ttu-id="79d23-117">Moniteur réseau stocke la liste des protocoles qui suivent dans la section du jeu de remise du fichier INI de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="79d23-117">Network Monitor stores the list of protocols that follow in the handoff set section of the parser INI file.</span></span>

<span data-ttu-id="79d23-118">Moniteur réseau stocke les informations du jeu de remise dans le fichier INI de l’analyseur, mais l’analyseur n’accède pas directement aux fichiers INI.</span><span class="sxs-lookup"><span data-stu-id="79d23-118">Network Monitor stores the handoff set information in the parser INI file, but the parser does not access the INI files directly.</span></span> <span data-ttu-id="79d23-119">Pour utiliser les informations du jeu de remise, l’analyseur appelle la fonction [**CreateHandoffTable**](createhandofftable.md) pour créer une table de remise.</span><span class="sxs-lookup"><span data-stu-id="79d23-119">To use the information in the handoff set, the parser calls the [**CreateHandoffTable**](createhandofftable.md) function to create a handoff table.</span></span> <span data-ttu-id="79d23-120">En règle générale, la table de remise est créée lorsque l’analyseur enregistre le protocole.</span><span class="sxs-lookup"><span data-stu-id="79d23-120">Typically, the handoff table is created when the parser registers the protocol.</span></span> <span data-ttu-id="79d23-121">Une fois le protocole inscrit, Moniteur réseau crée une table de jeu de remise que l’analyseur peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="79d23-121">After the protocol is registered, Network Monitor creates a handoff set table that the parser can use.</span></span>

<span data-ttu-id="79d23-122">L’analyseur utilise son jeu de remise lors de la reconnaissance des données.</span><span class="sxs-lookup"><span data-stu-id="79d23-122">The parser uses its handoff set when recognizing data.</span></span> <span data-ttu-id="79d23-123">Tout d’abord, l’analyseur lit la valeur de la propriété qui identifie le protocole suivant.</span><span class="sxs-lookup"><span data-stu-id="79d23-123">First the parser reads the value of the property that identifies the next protocol.</span></span> <span data-ttu-id="79d23-124">L’analyseur appelle ensuite [**GetProtocolFromTable**](getprotocolfromtable.md) pour obtenir un handle vers le protocole suivant.</span><span class="sxs-lookup"><span data-stu-id="79d23-124">Then the parser calls the [**GetProtocolFromTable**](getprotocolfromtable.md) to get a handle to the next protocol.</span></span> <span data-ttu-id="79d23-125">Enfin, l’analyseur retourne un pointeur vers le descripteur dans le paramètre *phNextProtocol* de [**RecognizeFrame**](recognizeframe.md).</span><span class="sxs-lookup"><span data-stu-id="79d23-125">Last, the parser returns a pointer to the handle in the *phNextProtocol* parameter of [**RecognizeFrame**](recognizeframe.md).</span></span>

 

 



