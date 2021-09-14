---
description: Un fournisseur de propriétés utilise les méthodes IWbemPropertyProvider comme interface principale de WMI. Avec IWbemPropertyProvider, vous pouvez implémenter le code pour récupérer et modifier des propriétés de classe et d’instance.
ms.assetid: d08c2ca4-9f8a-4a27-80fc-688d7c56f5eb
ms.tgt_platform: multiple
title: Implémentation de l’interface principale pour un fournisseur de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942117547380000e0da7d22a5e933cba4b3ffced
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915776"
---
# <a name="implementing-the-primary-interface-for-a-property-provider"></a>Implémentation de l’interface principale pour un fournisseur de propriétés

Un fournisseur de propriétés utilise les méthodes [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) comme interface principale de WMI. Avec **IWbemPropertyProvider**, vous pouvez implémenter le code pour récupérer et modifier des propriétés de classe et d’instance.

Le tableau suivant répertorie les méthodes [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) que vous pouvez implémenter pour un fournisseur de propriétés.



| Méthode                                                   | Fonctionnalité      |
|----------------------------------------------------------|--------------|
| [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) | Récupération    |
| [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) | Modification |



 

> [!Note]  
> Vous devez implémenter un fournisseur de propriétés en tant que fournisseur in-process. WMI initialise les fournisseurs de propriétés écrits comme des services ou des fichiers exécutables, mais n’appelle jamais leurs méthodes [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) et [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) .

 

Si vous choisissez de ne pas prendre en charge l’une de ces méthodes, votre fournisseur peut fournir une implémentation de stub qui retourne le **\_ fournisseur E WBEM \_ \_ non \_ compatible**.

Un fournisseur de propriétés identifie une classe ou une instance managée par un ensemble de trois qualificateurs : **PropertyContext**, **InstanceContext** et **ClassContext**. WMI passera des constantes de chaîne décrivant ces trois qualificateurs à votre fournisseur de propriétés.

Votre fournisseur de propriétés doit être prêt à gérer les types de qualificateurs de contexte suivants :

-   Le qualificateur **InstanceContext** est attaché à une instance et contient des informations qui s’appliquent à chaque propriété de l’instance.
-   Le qualificateur **ClassContext** est attaché à une classe et contient des informations qui s’appliquent à chaque instance de la classe. Par exemple, dans une classe utilisée pour stocker les données fournies par le fournisseur de Registre, **ClassContext** peut être le chemin d’accès à la clé de Registre qui contient les propriétés à signaler.
-   Le qualificateur **PropertyContext** spécifie les informations spécifiques au contexte qui se rapportent à la propriété. Par exemple, dans une classe utilisée pour stocker les données fournies par le fournisseur de Registre, **PropertyContext** spécifie le nom de la valeur de Registre à stocker par la propriété.

Ces qualificateurs peuvent fonctionner ensemble. Vous pouvez désigner une valeur **InstanceContext** et **PropertyContext** pour indiquer au fournisseur comment traiter des types particuliers d’instances. Par exemple, vous pouvez marquer les instances que le fournisseur reconnaît comme étant lisibles, mais n’a qu’une seule propriété accessible en écriture.

Le qualificateur le plus courant utilisé est **PropertyContext**. Par conséquent, WMI fournit le qualificateur **DynProps** comme raccourci. WMI considère que chaque propriété d’une instance marquée avec **DynProps** a également les qualificateurs **dynamiques**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)et **PropertyContext** .

 

 



