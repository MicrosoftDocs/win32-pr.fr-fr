---
description: Pour créer un fournisseur de propriétés WMI, vous devez inscrire l' \_ \_ instance Win32Provider qui représente votre fournisseur à l’aide d’une instance de \_ \_ PropertyProviderRegistration.
ms.assetid: e7e30acc-ea41-41e2-9bb3-cd931e8d799e
ms.tgt_platform: multiple
title: Inscription d’un fournisseur de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d56d91e3c2a45b0ad0fe83cf6b2bc32ab4353a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202179"
---
# <a name="registering-a-property-provider"></a>Inscription d’un fournisseur de propriétés

Pour créer un [*fournisseur de propriétés*](gloss-p.md) WMI, vous devez inscrire l’instance [**\_ \_ Win32Provider**](--win32provider.md) qui représente votre fournisseur à l’aide d’une instance de [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md). En tant qu’objet COM, votre fournisseur doit s’inscrire auprès du système d’exploitation et de WMI. La procédure suivante suppose que vous avez déjà implémenté le processus d’inscription, comme décrit dans [inscription d’un fournisseur](registering-a-provider.md).

La procédure suivante décrit comment inscrire un fournisseur de propriétés.

**Pour inscrire un fournisseur de propriétés**

1.  Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) qui décrit le fournisseur de propriétés.

    La classe [**\_ \_ Win32Provider**](--win32provider.md) accepte les valeurs par défaut pour les autres propriétés, telles que la valeur **true** pour la propriété **pure** . Pour plus d’informations, consultez [**\_ \_ Win32Provider**](--win32provider.md).

2.  Créez une instance de la classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) qui décrit l’ensemble des fonctionnalités du fournisseur.

    La classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) hérite de nombreuses propriétés de la classe parente [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , qui fournit des valeurs booléennes qui indiquent la prise en charge de fonctionnalités particulières et un tableau de chaînes pour indiquer la prise en charge des requêtes.

    Veillez à baliser la classe avec les qualificateurs [**Dynamic**](dynamic-qualifier.md) et [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) . Le qualificateur **dynamique** indique que WMI doit utiliser un fournisseur dynamique pour récupérer les instances de classe qui contiennent les propriétés prises en charge. Le qualificateur du **fournisseur** spécifie le nom du fournisseur que WMI doit utiliser.

WMI appelle NewQuery sur un fournisseur d’événements lorsqu’un consommateur client inscrit une requête de filtre d’événement qui contient des références aux événements pris en charge par ce fournisseur d’événements. Ainsi, le fournisseur d’événements responsable des événements de modification d’instance pour la classe EmailClass peut être configuré pour générer des notifications uniquement pour l’expéditeur. Lorsque le fournisseur reçoit une requête demandant la notification des modifications apportées à la propriété Subject, le fournisseur peut commencer à générer ces notifications. Dans ce scénario, WMI n’est pas obligé d’ignorer les notifications qui modifient uniquement les destinataires du rapport.

L’exemple de code MOF suivant décrit des instances qui peuvent être utilisées pour inscrire un fournisseur de propriétés.

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "PropProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __PropertyProviderRegistration
  {
    Provider = $P;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
  };
```

> [!Note]  
> Seuls les administrateurs peuvent inscrire ou supprimer un fournisseur de propriétés en créant une instance de [**\_ \_ Win32Provider**](--win32provider.md) et [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md).

 

 

 



