---
title: " dans, size_is et out, size_is prototype"
description: Le prototype de fonction suivant utilise deux chaînes comptées. Le développeur doit écrire du code sur le client et sur le serveur pour effectuer le suivi des longueurs de tableau de caractères et transmettre des paramètres qui indiquent aux stub le nombre d’éléments de tableau à transmettre.
ms.assetid: 334c5e0f-b1fb-41ca-8157-d92525e78b3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d03dbb4dd65d44122bea7ff086013295e0bf616d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382623"
---
# <a name="in-size_is-and-out-size_is-prototype"></a><span data-ttu-id="d9ad6-104">\[dans, la taille \_ est \] et \[ sortante, la taille \_ est un \] prototype</span><span class="sxs-lookup"><span data-stu-id="d9ad6-104">\[in, size\_is\] and \[out, size\_is\] Prototype</span></span>

<span data-ttu-id="d9ad6-105">Le prototype de fonction suivant utilise deux chaînes comptées.</span><span class="sxs-lookup"><span data-stu-id="d9ad6-105">The following function prototype uses two counted strings.</span></span> <span data-ttu-id="d9ad6-106">Le développeur doit écrire du code sur le client et sur le serveur pour effectuer le suivi des longueurs de tableau de caractères et transmettre des paramètres qui indiquent aux stub le nombre d’éléments de tableau à transmettre.</span><span class="sxs-lookup"><span data-stu-id="d9ad6-106">The developer must write code on both client and server to keep track of the character array lengths and pass parameters that tell the stubs how many array elements to transmit.</span></span>

``` syntax
void Analyze(
    [in,  length_is(cbIn), size_is(STRSIZE)]    char  achIn[],
    [in]                                        long  cbIn,
    [out, length_is(*pcbOut), size_is(STRSIZE)] char  achOut[],
    [out]                                       long *pcbOut);
```

<span data-ttu-id="d9ad6-107">Notez que les paramètres qui décrivent la longueur du tableau sont transmis dans la même direction que les *tableaux : les* paramètres de la table de base de *achIn* sont des paramètres, \[ [](/windows/desktop/Midl/in) \] tandis que *pcbOut* et *achOut* sont des paramètres de \[ [**sortie**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="d9ad6-107">Note the parameters that describe the array length are transmitted in the same direction as the arrays: *cbIn* and *achIn* are \[[**in**](/windows/desktop/Midl/in)\] parameters while *pcbOut* and *achOut* are \[[**out**](/windows/desktop/Midl/out-idl)\] parameters.</span></span> <span data-ttu-id="d9ad6-108">En tant que paramètre de **\[ \] sortie** , le paramètre *PcbOut* doit suivre la Convention C et être déclaré comme pointeur.</span><span class="sxs-lookup"><span data-stu-id="d9ad6-108">As an **\[out\]** parameter, the parameter *pcbOut* must follow C convention and be declared as a pointer.</span></span>

<span data-ttu-id="d9ad6-109">Le code client compte le nombre de caractères de la chaîne, y compris le zéro de fin, avant d’appeler la procédure distante comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="d9ad6-109">The client code counts the number of characters in the string, including the trailing zero, before calling the remote procedure as shown:</span></span>

``` syntax
/* client */
char achIn[STRSIZE], achOut[STRSIZE];
long cbIn, cbOut;
...
gets_s(achIn, STRSIZE);                   // get patient input
cbIn = strlen(achIn) + 1;      // transmitted elements
Analyze(achIn, cbIn, achOut, &cbOut);
```

<span data-ttu-id="d9ad6-110">La procédure distante sur le serveur fournit la longueur de la mémoire tampon de retour dans *cbOut* , comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="d9ad6-110">The remote procedure on the server supplies the length of the return buffer in *cbOut* as shown:</span></span>

``` syntax
/* server */
void Analyze(char *pchIn,
             long cbIn,
             char *pchOut,
             long *pcbOut)
{
   ...
   *pcbOut = strlen(pchOut) + 1; // transmitted elements
   return;
}
```

<span data-ttu-id="d9ad6-111">L' \[ attribut de **chaîne** \] peut être utilisé lorsqu’un paramètre est considéré comme une chaîne.</span><span class="sxs-lookup"><span data-stu-id="d9ad6-111">The \[**string**\] attribute can be utilized when a parameter is known to be a string.</span></span> <span data-ttu-id="d9ad6-112">Cet attribut indique au stub de calculer la taille de la chaîne, ce qui élimine la surcharge associée à la \[ [**longueur**](/windows/desktop/Midl/size-is) des \] paramètres.</span><span class="sxs-lookup"><span data-stu-id="d9ad6-112">This attribute directs the stub to calculate the string size, thus eliminating the overhead associated with the \[[**length is**](/windows/desktop/Midl/size-is)\] parameters.</span></span> <span data-ttu-id="d9ad6-113">En outre, il dirige le stub pour vérifier que la chaîne se termine par **null** avant de passer le paramètre à l’application.</span><span class="sxs-lookup"><span data-stu-id="d9ad6-113">Additionally, it will direct the stub to verify the string is **NULL** terminated before passing the parameter to the application.</span></span>

 

 