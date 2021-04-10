---
description: Les actions personnalisées ICE communiquent en appelant MsiProcessMessage et en publiant un \_ message de type utilisateur INSTALLMESSAGE.
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: Instructions relatives aux messages ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4bee7dbf22184883e49da4d5a5f66f9debb577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951135"
---
# <a name="ice-message-guidelines"></a><span data-ttu-id="985d7-103">Instructions relatives aux messages ICE</span><span class="sxs-lookup"><span data-stu-id="985d7-103">ICE Message Guidelines</span></span>

<span data-ttu-id="985d7-104">Les actions personnalisées ICE communiquent en appelant [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) et en publiant un \_ message de type utilisateur INSTALLMESSAGE.</span><span class="sxs-lookup"><span data-stu-id="985d7-104">ICE custom actions communicate by calling [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) and posting an INSTALLMESSAGE\_USER type message.</span></span>

<span data-ttu-id="985d7-105">Lors de la création d’une chaîne de message pour une action personnalisée ICE, mettez en forme la chaîne comme suit.</span><span class="sxs-lookup"><span data-stu-id="985d7-105">When authoring a message string for an ICE custom action, format the string as follows.</span></span>

<span data-ttu-id="985d7-106">*Nom de la glace* <tab> *Type* <tab> de message *Description* <tab> *URL ou emplacement* <tab> d’aide Nom de la *table* <tab> Nom de la *colonne* <tab> *Clé primaire* <tab> *Clé primaire* <tab> *Clé primaire* .</span><span class="sxs-lookup"><span data-stu-id="985d7-106">*Name of ICE* <tab> *Message Type* <tab> *Description* <tab> *Help URL or location* <tab> *Table Name* <tab> *Column Name* <tab> *Primary Key* <tab> *Primary Key* <tab> *Primary Key* .</span></span> <span data-ttu-id="985d7-107">.</span><span class="sxs-lookup"><span data-stu-id="985d7-107">.</span></span> <span data-ttu-id="985d7-108">.</span><span class="sxs-lookup"><span data-stu-id="985d7-108">.</span></span> <span data-ttu-id="985d7-109">(répétez cette opération pour autant de clés primaires que nécessaire)</span><span class="sxs-lookup"><span data-stu-id="985d7-109">(repeat for as many primary keys as needed)</span></span>

<span data-ttu-id="985d7-110">Les trois premiers champs de la chaîne sont requis dans chaque message.</span><span class="sxs-lookup"><span data-stu-id="985d7-110">The first three fields of the string are required in every message.</span></span>

<span data-ttu-id="985d7-111">Le champ type de message spécifie si la glace signale un message d’erreur, d’erreur, d’avertissement ou d’information.</span><span class="sxs-lookup"><span data-stu-id="985d7-111">The Message Type field specifies whether the ICE reports a Failure, Error, Warning, or Informational message.</span></span>



| <span data-ttu-id="985d7-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="985d7-112">Value</span></span> | <span data-ttu-id="985d7-113">type de message</span><span class="sxs-lookup"><span data-stu-id="985d7-113">Message type</span></span>                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="985d7-114">0</span><span class="sxs-lookup"><span data-stu-id="985d7-114">0</span></span>     | <span data-ttu-id="985d7-115">Message d’échec signalant l’échec de l’action personnalisée ICE.</span><span class="sxs-lookup"><span data-stu-id="985d7-115">Failure message reporting the failure of the ICE custom action.</span></span>                                                                                                       |
| <span data-ttu-id="985d7-116">1</span><span class="sxs-lookup"><span data-stu-id="985d7-116">1</span></span>     | <span data-ttu-id="985d7-117">Message d’erreur lors de la création de la base de données qui provoque un comportement incorrect.</span><span class="sxs-lookup"><span data-stu-id="985d7-117">Error message reporting database authoring that cause incorrect behavior.</span></span>                                                                                             |
| <span data-ttu-id="985d7-118">2</span><span class="sxs-lookup"><span data-stu-id="985d7-118">2</span></span>     | <span data-ttu-id="985d7-119">Message d’avertissement création de la base de données qui provoque un comportement incorrect dans certains cas.</span><span class="sxs-lookup"><span data-stu-id="985d7-119">Warning message reporting database authoring that causes incorrect behavior in certain cases.</span></span> <span data-ttu-id="985d7-120">Les avertissements peuvent également signaler des effets secondaires inattendus de la création de bases de données.</span><span class="sxs-lookup"><span data-stu-id="985d7-120">Warnings can also report unexpected side-effects of database authoring.</span></span> |
| <span data-ttu-id="985d7-121">3</span><span class="sxs-lookup"><span data-stu-id="985d7-121">3</span></span>     | <span data-ttu-id="985d7-122">Message d’information.</span><span class="sxs-lookup"><span data-stu-id="985d7-122">Informational message.</span></span>                                                                                                                                                |



 

<span data-ttu-id="985d7-123">Si l’aide n’est pas disponible, le champ URL d’aide peut être une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="985d7-123">If help is not available, the Help URL field may be the empty string.</span></span>

<span data-ttu-id="985d7-124">Les messages d’erreur et d’avertissement doivent fournir le nom de la table, le nom de la colonne et les champs de clé primaire.</span><span class="sxs-lookup"><span data-stu-id="985d7-124">Error and Warning messages should provide the Table Name, Column Name, and Primary Key fields.</span></span> <span data-ttu-id="985d7-125">Si l’un de ces champs est omis, tous les champs qui suivent le premier champ vide doivent être ignorés dans le message.</span><span class="sxs-lookup"><span data-stu-id="985d7-125">If any of these fields are omitted, all of the fields following the first blank field must be left out of the message.</span></span> <span data-ttu-id="985d7-126">Par exemple, un nom de table est fourni sans nom de colonne ni clé primaire, ni nom de table et un nom de colonne est fourni sans clé primaire.</span><span class="sxs-lookup"><span data-stu-id="985d7-126">For example, a table name is provided without a column name and primary keys or a table name and a column name is provided with no primary keys.</span></span> <span data-ttu-id="985d7-127">Toutefois, un nom de colonne et des clés primaires ne peuvent pas être utilisés sans nom de table.</span><span class="sxs-lookup"><span data-stu-id="985d7-127">However a column name and primary keys cannot be used without a table name.</span></span> <span data-ttu-id="985d7-128">Plusieurs clés primaires peuvent être listées jusqu’à ce que toutes les clés primaires de cette table aient reçu des valeurs.</span><span class="sxs-lookup"><span data-stu-id="985d7-128">Multiple primary keys may be listed until all the primary keys in that table have been given values.</span></span>

## <a name="examples"></a><span data-ttu-id="985d7-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="985d7-129">Examples</span></span>

<span data-ttu-id="985d7-130">Premier message illustré par l' [exemple de code Ice en C++](sample-ice-in-c-.md):</span><span class="sxs-lookup"><span data-stu-id="985d7-130">The first message illustrated by the [Sample ICE in C++](sample-ice-in-c-.md):</span></span>

<span data-ttu-id="985d7-131">« ICE01 \\ T3 \\ TLA 04/29/1998 par <insérer le nom de l’auteur ici> ».</span><span class="sxs-lookup"><span data-stu-id="985d7-131">"ICE01\\t3\\tCreated 04/29/1998 by <insert author's name here>."</span></span>

<span data-ttu-id="985d7-132">Deuxième message publié par l’exemple de code ICE :</span><span class="sxs-lookup"><span data-stu-id="985d7-132">The second message posted by the sample ICE:</span></span>

<span data-ttu-id="985d7-133">« ICE01 \\ T3 \\ tLast a modifié 05/06/1999 en <insérer le nom de l’auteur ici> ».</span><span class="sxs-lookup"><span data-stu-id="985d7-133">"ICE01\\t3\\tLast modified 05/06/1999 by <insert author's name here>."</span></span>

<span data-ttu-id="985d7-134">Troisième message publié par l’exemple de code ICE.</span><span class="sxs-lookup"><span data-stu-id="985d7-134">The third message posted by the sample ICE.</span></span>

<span data-ttu-id="985d7-135">« ICE01 \\ T3 \\ tSimple Ice à illustrer le concept de glace ».</span><span class="sxs-lookup"><span data-stu-id="985d7-135">"ICE01\\t3\\tSimple ICE to illustrating the ICE concept".</span></span>

 

 



