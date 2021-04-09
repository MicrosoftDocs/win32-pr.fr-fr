---
description: La table ReserveCost est une table facultative qui permet à l’auteur de réserver une quantité d’espace disque dans un répertoire qui dépend de l’état d’installation d’un composant.
ms.assetid: 371e72f1-40a2-4ed2-b0ab-33840075ff47
title: Table ReserveCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f593fd11789cd2304385b97e96e50a009fbde0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952230"
---
# <a name="reservecost-table"></a>Table ReserveCost

La table ReserveCost est une table facultative qui permet à l’auteur de réserver une quantité d’espace disque dans un répertoire qui dépend de l’état d’installation d’un composant.

La table ReserveCost contient les colonnes suivantes.



| Colonne        | Type                               | Clé | Nullable |
|---------------|------------------------------------|-----|----------|
| ReserveKey    | [Identificateur](identifier.md)       | O   | N        |
| -\_   | [Identificateur](identifier.md)       | N   | N        |
| ReserveFolder | [Identificateur](identifier.md)       | N   | O        |
| ReserveLocal  | [DoubleInteger](doubleinteger.md) | N   | N        |
| ReserveSource | [DoubleInteger](doubleinteger.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey
</dt> <dd>

Clé primaire qui identifie de façon unique une entrée de table ReserveCost.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe vers la colonne de l’une des tables de [composants](component-table.md) . Réserve une quantité d’espace spécifiée si ce composant doit être installé.

</dd> <dt>

<span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder
</dt> <dd>

Cette colonne contient le nom d’une propriété qui est le chemin d’accès complet au répertoire de destination. Ce nom de propriété est généralement le nom d’un répertoire dans la table de [répertoire](directory-table.md) ou le nom d’un jeu de propriétés obtenu à l’aide de l’action [AppSearch](appsearch-action.md) . Cela ajoute la quantité d’espace disque spécifiée dans ReserveLocal ou ReserveSource au coût du volume de l’appareil contenant le répertoire.

</dd> <dt>

<span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal
</dt> <dd>

Nombre d’octets d’espace disque à réserver si le composant lié est installé pour s’exécuter localement.

</dd> <dt>

<span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ReserveSource
</dt> <dd>

Nombre d’octets d’espace disque à réserver si le composant lié est installé pour s’exécuter à partir de la source.

</dd> </dl>

## <a name="remarks"></a>Notes

La réservation de coûts de cette façon peut être utile pour les auteurs qui souhaitent s’assurer qu’une quantité minimale d’espace disque sera disponible une fois l’installation terminée. Par exemple, cet espace disque peut être réservé pour les documents utilisateur ou pour les fichiers d’application (tels que les fichiers d’index) qui sont créés uniquement après le démarrage de l’application après l’installation.

Vous pouvez utiliser la table ReserveCost pour permettre aux actions personnalisées de spécifier un coût approximatif pour tous les fichiers, entrées de registre ou autres éléments que l’action personnalisée peut installer. Les actions personnalisées qui ajoutent des entrées à la table ReserveCost doivent être séquencées entre les actions [CostInitialize](costinitialize-action.md) et [FileCost](filecost-action.md) . Cela est nécessaire pour que l’action FileCost Initialise correctement les coûts de tous les composants affectés par les entrées de la table ReserveCost.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



