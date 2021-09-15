---
description: Moniteur réseau charge une capture à partir du fichier de capture, puis démarre l’appel de la fonction Register pour tous les protocoles qu’elle peut identifier. Chaque DLL de l’analyseur doit implémenter une fonction d’inscription pour chaque protocole pris en charge par la DLL de l’analyseur.
ms.assetid: a53c64cb-569f-454b-ae85-7b850228c954
title: Implémentation du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59f34f5f97925627184db7188aac0a9eb796a7d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238421"
---
# <a name="implementing-register"></a>Implémentation du Registre

Moniteur réseau charge une capture à partir du fichier de capture, puis démarre l’appel de la fonction [**Register**](register-parser.md) pour tous les protocoles qu’elle peut identifier. Chaque DLL de l’analyseur doit implémenter une fonction d' **inscription** pour chaque protocole pris en charge par la dll de l’analyseur.

Chaque implémentation de la [**fonction Register**](register-parser.md) doit appeler les [**fonctions CreatePropertyDatabase**](createpropertydatabase.md) et [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) pour créer et remplir la [*base de données de propriétés*](p.md) pour le protocole, puis le [**CreateHandoffTable**](createhandofftable.md) pour créer la [*table de remise*](h.md) pour le protocole, si nécessaire.

> [!Note]  
> Les propriétés de protocole sont définies pour Moniteur réseau. Les propriétés ne sont pas mappées à un emplacement dans une capture de données jusqu’à ce que la fonction d’exportation [**AttachProperties**](attachproperties.md) soit appelée.

 

La procédure suivante identifie les étapes nécessaires pour implémenter la fonction [**Register**](register-parser.md) .

**Pour implémenter Register pour un protocole**

1.  Définissez un tableau de structures [**PROPERTYINFO**](propertyinfo.md) pour décrire chaque propriété prise en charge par le protocole.
2.  Appelez [**CreatePropertyDatabase**](createpropertydatabase.md) pour fournir un handle de protocole et le nombre de propriétés prises en charge par le protocole.
3.  Appelez [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) dans une boucle pour ajouter chaque propriété définie dans le tableau de structures [**PROPERTYINFO**](propertyinfo.md) .
4.  Si le protocole utilise une table de remise, appelez [**CreateHandoffTable**](createhandofftable.md): une fois que toutes les propriétés du protocole sont ajoutées à la base de données des propriétés.

Voici une implémentation de base de la commande [**Register**](register-parser.md). Notez qu’une base de données de propriétés est créée pour un protocole qui prend en charge uniquement deux propriétés. Cet exemple de code est extrait de l’analyseur générique fourni par Moniteur réseau.

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

 

 
