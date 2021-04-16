---
title: Out-Only paramètres de pointeur unique ou complet non acceptés
description: Les pointeurs uniques ou complets qui ne sont pas acceptés par le compilateur MIDL ne sont pas acceptés. De telles spécifications provoquent la génération d’un message d’erreur par le compilateur MIDL.
ms.assetid: 0477980e-d76e-452f-9ab1-71a8ed8642d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b21baa370c1b68fb3c708a8fdb21115686646f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508041"
---
# <a name="out-only-unique-or-full-pointer-parameters-not-accepted"></a><span data-ttu-id="395e5-104">Out-Only paramètres de pointeur unique ou complet non acceptés</span><span class="sxs-lookup"><span data-stu-id="395e5-104">Out-Only Unique or Full Pointer Parameters Not Accepted</span></span>

<span data-ttu-id="395e5-105">Les pointeurs uniques ou complets qui sont en \[ [dehors](/windows/desktop/Midl/out-idl) \] de ne sont pas acceptés par le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="395e5-105">Unique or full pointers that are \[ [out](/windows/desktop/Midl/out-idl)\]-only are not accepted by the MIDL compiler.</span></span> <span data-ttu-id="395e5-106">De telles spécifications provoquent la génération d’un message d’erreur par le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="395e5-106">Such specifications cause the MIDL compiler to generate an error message.</span></span>

<span data-ttu-id="395e5-107">Le stub serveur généré automatiquement doit allouer de la mémoire pour le référent du pointeur afin que l’application serveur puisse stocker des données dans cette zone mémoire.</span><span class="sxs-lookup"><span data-stu-id="395e5-107">The automatically generated server stub has to allocate memory for the pointer referent so that the server application can store data in that memory area.</span></span> <span data-ttu-id="395e5-108">En fonction de la définition d’un paramètre en **\[ sortie \]** seule, aucune information sur le paramètre n’est transmise du client au serveur.</span><span class="sxs-lookup"><span data-stu-id="395e5-108">According to the definition of an **\[out\]**-only parameter, no information about the parameter is transmitted from client to server.</span></span> <span data-ttu-id="395e5-109">Dans le cas d’un pointeur unique, qui peut prendre la valeur null, le stub du serveur ne dispose pas de suffisamment d’informations pour dupliquer correctement le pointeur unique dans l’espace d’adressage du serveur, et le stub ne peut pas non plus indiquer si le pointeur doit pointer vers une adresse valide ou s’il doit avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="395e5-109">In the case of a unique pointer, which can take the value null, the server stub does not have enough information to correctly duplicate the unique pointer in the server's address space, nor does the stub have any information about whether the pointer should point to a valid address or whether it should be set to null.</span></span> <span data-ttu-id="395e5-110">Par conséquent, cette combinaison n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="395e5-110">Therefore, this combination is not allowed.</span></span>

<span data-ttu-id="395e5-111">Plutôt que de \[ **sortir**, [uniques](/windows/desktop/Midl/unique) \] ou \[ **sortants** des pointeurs [ptr](/windows/desktop/Midl/ptr) \] , utilisez \[ **des** pointeurs in, **out**, **unique** \] ou \[ **in**, **out**, **ptr** \] , ou utilisez un autre niveau d’indirection, tel qu’un pointeur de référence qui pointe vers le pointeur unique ou complet valide.</span><span class="sxs-lookup"><span data-stu-id="395e5-111">Rather than \[**out**, [unique](/windows/desktop/Midl/unique)\] or \[**out**, [ptr](/windows/desktop/Midl/ptr)\] pointers, use \[**in**, **out**, **unique**\] or \[**in**, **out**, **ptr**\] pointers, or use another level of indirection such as a reference pointer that points to the valid unique or full pointer.</span></span>

 

 