---
title: Interface IAccessibleEx
description: Les contrôles qui n’ont pas de fournisseur UI Automation Microsoft, mais qui implémentent IAccessible, peuvent facilement être mis à niveau pour fournir une fonctionnalité d’automatisation d’interface utilisateur en implémentant l’interface IAccessibleEx.
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a74e7d464acf18244d91bc69199a56004b20beb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013163"
---
# <a name="the-iaccessibleex-interface"></a>Interface IAccessibleEx

Les contrôles qui n’ont pas de fournisseur UI Automation Microsoft, mais qui implémentent [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), peuvent facilement être mis à niveau pour fournir une fonctionnalité d’automatisation d’interface utilisateur en implémentant l’interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Cette interface permet au contrôle d’exposer des propriétés UI Automation et des modèles de contrôle, sans avoir besoin d’une implémentation complète des interfaces du fournisseur UI Automation telles que [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment). Pour utiliser **IAccessibleEx**, **IRawElementProviderFragment** et toutes les autres interfaces UI Automation, incluez le fichier d’en-tête uiautomation. h dans votre code source.

Par exemple, considérez un contrôle personnalisé qui a une valeur de plage. Le serveur Microsoft Active Accessibility pour le contrôle définit le rôle du contrôle et est en mesure de retourner sa valeur actuelle. Toutefois, étant donné que Microsoft Active Accessibility ne définit pas de propriétés minimales et maximales, le serveur n’a pas la possibilité de retourner les valeurs minimale et maximale du contrôle. Un client UI Automation est en mesure de récupérer le rôle du contrôle, la valeur actuelle et d’autres propriétés de Active Accessibility Microsoft, car le noyau UI Automation peut les obtenir via [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Toutefois, sans accès à une interface [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) sur l’objet, UI Automation ne peut pas non plus récupérer les valeurs maximale et minimale.

Le développeur de contrôle peut fournir un fournisseur UI Automation complet pour le contrôle, mais cela signifierait la duplication d’une grande partie des fonctionnalités existantes de l’implémentation de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : par exemple, la navigation et les propriétés communes. Au lieu de cela, le développeur peut continuer à s’appuyer sur **IAccessible** pour fournir cette fonctionnalité, tout en ajoutant la prise en charge des propriétés spécifiques au contrôle par le biais de [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).

## <a name="in-this-section"></a>Dans cette section

-   [Instructions d’implémentation de IAccessibleEx](iaccessibleex-implementation-guidelines.md)
-   [Implémentation de IAccessibleEx pour les fournisseurs](implementing-iaccessibleex-for-providers.md)
-   [Utilisation de IAccessibleEx à partir d’un client](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Infrastructure commune](common-infrastructure.md)
</dt> </dl>

 

 




