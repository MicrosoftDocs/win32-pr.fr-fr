---
description: Moniteur réseau charge une capture à partir du fichier de capture, puis démarre l’appel de la fonction Register pour tous les protocoles qu’elle peut identifier. Chaque DLL de l’analyseur doit implémenter une fonction d’inscription pour chaque protocole pris en charge par la DLL de l’analyseur.
ms.assetid: a53c64cb-569f-454b-ae85-7b850228c954
title: Implémentation du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59f34f5f97925627184db7188aac0a9eb796a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521186"
---
# <a name="implementing-register"></a><span data-ttu-id="e2011-104">Implémentation du Registre</span><span class="sxs-lookup"><span data-stu-id="e2011-104">Implementing Register</span></span>

<span data-ttu-id="e2011-105">Moniteur réseau charge une capture à partir du fichier de capture, puis démarre l’appel de la fonction [**Register**](register-parser.md) pour tous les protocoles qu’elle peut identifier.</span><span class="sxs-lookup"><span data-stu-id="e2011-105">Network Monitor loads a capture from the capture file, and then starts calling the [**Register**](register-parser.md) function for all the protocols that it can identify.</span></span> <span data-ttu-id="e2011-106">Chaque DLL de l’analyseur doit implémenter une fonction d' **inscription** pour chaque protocole pris en charge par la dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="e2011-106">Each parser DLL must implement a **Register** function for each protocol that the parser DLL supports.</span></span>

<span data-ttu-id="e2011-107">Chaque implémentation de la [**fonction Register**](register-parser.md) doit appeler les [**fonctions CreatePropertyDatabase**](createpropertydatabase.md) et [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) pour créer et remplir la [*base de données de propriétés*](p.md) pour le protocole, puis le [**CreateHandoffTable**](createhandofftable.md) pour créer la [*table de remise*](h.md) pour le protocole, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e2011-107">Each implementation of the [**Register**](register-parser.md) function must call the [**CreatePropertyDatabase**](createpropertydatabase.md) and [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) functions to create and fill-in the [*property database*](p.md) for the protocol, and then the [**CreateHandoffTable**](createhandofftable.md) to create the [*handoff table*](h.md) for the protocol — if needed.</span></span>

> [!Note]  
> <span data-ttu-id="e2011-108">Les propriétés de protocole sont définies pour Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="e2011-108">Protocol properties are defined for Network Monitor.</span></span> <span data-ttu-id="e2011-109">Les propriétés ne sont pas mappées à un emplacement dans une capture de données jusqu’à ce que la fonction d’exportation [**AttachProperties**](attachproperties.md) soit appelée.</span><span class="sxs-lookup"><span data-stu-id="e2011-109">Properties are not mapped to a location in a capture data until the [**AttachProperties**](attachproperties.md) export function is called.</span></span>

 

<span data-ttu-id="e2011-110">La procédure suivante identifie les étapes nécessaires pour implémenter la fonction [**Register**](register-parser.md) .</span><span class="sxs-lookup"><span data-stu-id="e2011-110">The following procedure identifies the steps necessary to implement the [**Register**](register-parser.md) function.</span></span>

<span data-ttu-id="e2011-111">**Pour implémenter Register pour un protocole**</span><span class="sxs-lookup"><span data-stu-id="e2011-111">**To implement Register for one protocol**</span></span>

1.  <span data-ttu-id="e2011-112">Définissez un tableau de structures [**PROPERTYINFO**](propertyinfo.md) pour décrire chaque propriété prise en charge par le protocole.</span><span class="sxs-lookup"><span data-stu-id="e2011-112">Define an array of [**PROPERTYINFO**](propertyinfo.md) structures to describe each property that the protocol supports.</span></span>
2.  <span data-ttu-id="e2011-113">Appelez [**CreatePropertyDatabase**](createpropertydatabase.md) pour fournir un handle de protocole et le nombre de propriétés prises en charge par le protocole.</span><span class="sxs-lookup"><span data-stu-id="e2011-113">Call [**CreatePropertyDatabase**](createpropertydatabase.md) to provide a protocol handle, and the number of properties that the protocol supports.</span></span>
3.  <span data-ttu-id="e2011-114">Appelez [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) dans une boucle pour ajouter chaque propriété définie dans le tableau de structures [**PROPERTYINFO**](propertyinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="e2011-114">Call [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) in a loop to add each property defined in the [**PROPERTYINFO**](propertyinfo.md) structure array.</span></span>
4.  <span data-ttu-id="e2011-115">Si le protocole utilise une table de remise, appelez [**CreateHandoffTable**](createhandofftable.md): une fois que toutes les propriétés du protocole sont ajoutées à la base de données des propriétés.</span><span class="sxs-lookup"><span data-stu-id="e2011-115">If the protocol uses a handoff table, call [**CreateHandoffTable**](createhandofftable.md)— after all the properties of the protocol are added to the property database.</span></span>

<span data-ttu-id="e2011-116">Voici une implémentation de base de la commande [**Register**](register-parser.md).</span><span class="sxs-lookup"><span data-stu-id="e2011-116">The following is a basic implementation of [**Register**](register-parser.md).</span></span> <span data-ttu-id="e2011-117">Notez qu’une base de données de propriétés est créée pour un protocole qui prend en charge uniquement deux propriétés.</span><span class="sxs-lookup"><span data-stu-id="e2011-117">Note that a property database is created for a protocol that supports only two properties.</span></span> <span data-ttu-id="e2011-118">Cet exemple de code est extrait de l’analyseur générique fourni par Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="e2011-118">This code example is taken from the generic parser that Network Monitor provides.</span></span>

``` syntax
#include <windows.h>

PROPERTYINFO MyProtocolPropertyTable[]
{
  // Summary property (0)
  {
     0,                               // Handle to property.
     0,                               // Reserved.
     "Summary",                       // Property label.
     "Summary of protocol packet",    // Property comment.
     PROP_TYPE_SUMMARY,               // Data type of property.
     PROP_QUAL_NONE,                  // Data type qualifier.
     NULL,                            // Reserved.
     80,                              // 
     FormatPropertyInstance           // 
  }

  // WORD property (1)
  {
     0,                               // Handle to property.
     0,                               // Reserved.
     "WORD property",                 // Property label.
     "16-bit WORD property",         // Property comment.
     PROP_TYPE_WORD,                  // Data type of property.
     PROP_QUAL_NONE,                  // Data type qualifier.
     NULL,                            // Reserved.
     80,                              // 
     FormatPropertyInstance           // 
  }

}

void BHAPI MyProtocolRegister( HPPROTOCOL hProtocol) 
{
  // Create property database.
  DWORD dwNumberOfProperties = 2;
  CreatePropertyDatabase (hProtocol,
                          dwNumberOfProperties
                          );
  
  // Add properties to database.
  WORD i;
  for( i=0; i< dwNumberOfProperties; i++)
  {
     AddProperty(hProtocol, &MyProtocolPropertyTable[i]);
  }

  // Create handoff table.
  CreateHandoffTable("myProtocolHandoffTable",
                          "myProtocol.ini",
                           hTable,
                           MaxEntries,
                           10       // Handoff set values are base 10.
                          )
}
```

 

 
