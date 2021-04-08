---
title: Le modèle de programmation
description: Au début de la programmation informatique, chaque programme était écrit sous la forme d’un grand segment monolithique, rempli d’instructions goto.
ms.assetid: b64d5338-a06a-4a27-bedb-c9011fa5a5a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcc0fd51404290b3d673982001cb3ee91bf1747
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673462"
---
# <a name="the-programming-model"></a><span data-ttu-id="5f180-103">Le modèle de programmation</span><span class="sxs-lookup"><span data-stu-id="5f180-103">The Programming Model</span></span>

<span data-ttu-id="5f180-104">Au début de la programmation informatique, chaque programme était écrit sous la forme d’un grand segment monolithique, rempli d’instructions **goto** .</span><span class="sxs-lookup"><span data-stu-id="5f180-104">In the early days of computer programming, each program was written as a large monolithic chunk, filled with **goto** statements.</span></span> <span data-ttu-id="5f180-105">Chaque programme devait gérer ses propres entrées et sorties sur différents périphériques matériels.</span><span class="sxs-lookup"><span data-stu-id="5f180-105">Each program had to manage its own input and output to different hardware devices.</span></span> <span data-ttu-id="5f180-106">À mesure que la discipline de programmation a évolué, ce code monolithique a été organisé en procédures, avec les procédures les plus couramment utilisées dans les bibliothèques pour le partage et la réutilisation.</span><span class="sxs-lookup"><span data-stu-id="5f180-106">As the programming discipline matured, this monolithic code was organized into procedures, with the most commonly used procedures packed in libraries for sharing and reuse.</span></span>

![instructions goto monolithiques et procédures empaquetées dans des bibliothèques partagées](images/prog-a06.png)

<span data-ttu-id="5f180-108">Le langage de programmation C prend en charge la programmation orientée procédure.</span><span class="sxs-lookup"><span data-stu-id="5f180-108">The C programming language supports procedure-oriented programming.</span></span> <span data-ttu-id="5f180-109">En C, la procédure principale est associée à toutes les autres procédures en tant que cases noires.</span><span class="sxs-lookup"><span data-stu-id="5f180-109">In C, the main procedure relates to all other procedures as black boxes.</span></span> <span data-ttu-id="5f180-110">Par exemple, la procédure main ne peut pas déterminer comment les procédures A, B et X effectuent leur travail.</span><span class="sxs-lookup"><span data-stu-id="5f180-110">For example, the main procedure cannot find out how procedures A, B, and X do their work.</span></span> <span data-ttu-id="5f180-111">La procédure main n’appelle qu’une autre procédure. elle ne contient pas d’informations sur l’implémentation de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="5f180-111">The main procedure only calls another procedure; it has no information about how that procedure is implemented.</span></span>

![isolement des activités effectuées dans les procédures externes](images/prog-a08.png)

<span data-ttu-id="5f180-113">Les langages de programmation orientés procédure fournissent des mécanismes simples pour spécifier et écrire des procédures.</span><span class="sxs-lookup"><span data-stu-id="5f180-113">Procedure-oriented programming languages provide simple mechanisms for specifying and writing procedures.</span></span> <span data-ttu-id="5f180-114">Par exemple, le prototype de fonction C ANSI-standard est une construction utilisée pour spécifier le nom d’une procédure, le type du résultat qu’elle retourne (le cas échéant) et le nombre, la séquence et le type de ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="5f180-114">For example, the ANSI-standard C-function prototype is a construct used to specify the name of a procedure, the type of the result it returns (if any) and the number, sequence, and type of its parameters.</span></span> <span data-ttu-id="5f180-115">L’utilisation du prototype de fonction est un moyen formel de spécifier une interface entre des procédures.</span><span class="sxs-lookup"><span data-stu-id="5f180-115">Using the function prototype is a formal way to specify an interface between procedures.</span></span>

<span data-ttu-id="5f180-116">Microsoft RPC s’appuie sur ce modèle de programmation en permettant aux procédures, regroupées dans les interfaces, de résider dans des processus différents de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="5f180-116">Microsoft RPC builds on that programming model by allowing procedures, grouped together in interfaces, to reside in different processes than the caller.</span></span> <span data-ttu-id="5f180-117">Microsoft RPC ajoute également une approche plus formelle de la définition de la procédure qui permet à l’appelant et à la routine appelée d’adopter un contrat pour échanger des données à distance et appeler des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="5f180-117">Microsoft RPC also adds a more formal approach to procedure definition that allows the caller and the called routine to adopt a contract for remotely exchanging data and invoking functionality.</span></span> <span data-ttu-id="5f180-118">Dans le modèle de programmation Microsoft RPC, les appels de fonction traditionnels sont complétés par deux éléments supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="5f180-118">In the Microsoft RPC programming model, traditional function calls are supplemented with two additional elements.</span></span>

-   <span data-ttu-id="5f180-119">Le premier élément est un fichier. idl/. ACF qui décrit précisément le mécanisme d’échange de données et de passage de paramètres entre l’appelant et la procédure appelée.</span><span class="sxs-lookup"><span data-stu-id="5f180-119">The first element is an .idl/.acf file that precisely describes the data exchange and parameter-passing mechanism between the caller and called procedure.</span></span>
-   <span data-ttu-id="5f180-120">Le deuxième élément est un ensemble d’API d’exécution qui fournissent aux développeurs un contrôle granulaire de l’appel de procédure distante, y compris des aspects de sécurité, la gestion de l’État sur le serveur, la spécification des clients qui peuvent communiquer avec le serveur, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="5f180-120">The second element is a set of run-time APIs that provide developers with granular control of the remote procedure call, including security aspects, managing state on the server, specifying which clients can talk to the server, and so on.</span></span>

 

 




