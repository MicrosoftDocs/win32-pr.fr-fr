---
description: Les classes utilisées pour contenir les données de Registre sont définies avec plusieurs qualificateurs standard.
ms.assetid: d4786880-6c50-4e36-9a16-47de430e77a9
ms.tgt_platform: multiple
title: Définition d’une classe Registry avec des qualificateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45fdff611814eadbf57eabedf7444d098666918
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237102"
---
# <a name="defining-a-registry-class-with-qualifiers"></a>Définition d’une classe Registry avec des qualificateurs

Les classes utilisées pour contenir les données de Registre sont définies avec plusieurs qualificateurs standard.

La liste suivante répertorie les qualificateurs standard :

-   [](standard-wmi-qualifiers.md) [ **Fournisseur** et dynamique](/windows/desktop/api/Provider/nl-provider-provider)

    Vous pouvez attacher le qualificateur **dynamique** à une classe ou à une instance. Le qualificateur **dynamique** marque la classe ou l’instance comme gérée dynamiquement par un fournisseur. Lorsque **Dynamic** apparaît sur une classe ou une instance, le qualificateur du [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) doit également apparaître. Le qualificateur du **fournisseur** identifie le fournisseur particulier qui doit gérer l’instance ou la classe dynamique.

-   [ClassContext](standard-wmi-qualifiers.md)

    Le qualificateur **ClassContext** est attaché à une classe. Il spécifie le chemin d’accès à la clé de Registre qui contient les informations que la classe représente.

    Le qualificateur **ClassContext** a le format suivant.

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    La valeur de keyPath peut être longue si elle comprend des clés avec des sous-clés.

    L’exemple suivant montre le qualificateur **ClassContext** qui contient le chemin d’accès à un périphérique de transport d’ordinateur particulier.

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

Le modèle suivant pour une définition de classe illustre l’utilisation des qualificateurs **dynamiques**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)et **ClassContext** . Le fournisseur nommé par le qualificateur du **fournisseur** est le fournisseur de Registre du système d’instance. Sachez que les chemins de registre ne respectent pas la casse, comme les noms de qualificateurs.

``` syntax
[dynamic, provider("RegProv"), 
    ClassContext("local|hkey_local_machine\\software\\microsoft
    \\WBEM\\transports\\Network Transport Modules")]

class RegTrans
{
  [key] string  TransportsGUID;
  [PropertyContext("Name")] string Name;
  [PropertyContext("Independent")] uint32 Enabled;
};
```

Les applications de gestion peuvent également utiliser le fournisseur de Registre système pour récupérer et modifier des données de Registre pour une clé particulière.

 

 



