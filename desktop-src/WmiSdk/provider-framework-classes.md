---
description: Les classes WMI C++ qui font partie de l’infrastructure du fournisseur WMI sont maintenant considérées dans l’état final.
ms.assetid: 062a7724-0589-4e9d-af7a-39fd9c08e40b
ms.tgt_platform: multiple
title: Classes de l’infrastructure du fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1562d00e6b3b1563ece933ba7dd9361dd8a5d94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520998"
---
# <a name="provider-framework-classes"></a>Classes de l’infrastructure du fournisseur

\[Les classes WMI C++ qui font partie de l’infrastructure du fournisseur WMI sont maintenant considérées comme à l’état final et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

L’infrastructure de fournisseur implémente les classes suivantes.



| Framework (classe)                                | Description                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CFrameworkQuery**](/windows/desktop/api/FrQuery/nl-frquery-cframeworkquery)     | Contient des méthodes pour le traitement des requêtes.                                                                                                                                                                              |
| [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)                 | Contient des méthodes pour définir et récupérer des propriétés et est une encapsulation de l’interface [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) . L’implémenteur ne doit pas avoir à accéder directement aux méthodes **IWbemClassObject** . |
| [**CThreadBase**](/windows/desktop/api/ThrdBase/nl-thrdbase-cthreadbase)             | Classe de base qui fournit les mécanismes internes de sécurité des threads pour l’infrastructure de fournisseur WMI.                                                                                                                    |
| [**CWbemGlueFactory**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemgluefactory)   | Partie de l’infrastructure du fournisseur WMI. L’infrastructure de fournisseur implémente les méthodes de cette interface en interne pour créer de nouvelles instances de classes pour le fournisseur.                                                     |
| [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) | Implémente [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) et les méthodes qui contrôlent le chargement et le déchargement du fournisseur Framework.                                                                             |
| [**Fournisseur**](/windows/desktop/api/Provider/nl-provider-provider)                   | Contient des fonctions d’assistance et fournit des implémentations par défaut des méthodes de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).                                                                                            |



 

Notez que la plupart des méthodes de l’infrastructure utilisent des paramètres [**CHString**](chstring.md) . **CHString** prend en charge plusieurs méthodes et propriétés identiques à celles de la Microsoft Foundation classes (MFC), mais sans la surcharge de MFC. Pour plus d’informations sur **CHString**, consultez Référence de la **classe CHString**.

 

 
