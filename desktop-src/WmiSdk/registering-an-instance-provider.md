---
description: Pour créer un fournisseur d’instances WMI, vous devez inscrire l' \_ \_ instance Win32Provider qui représente votre fournisseur à l’aide d’une instance de \_ \_ InstanceProviderRegistration.
ms.assetid: 5ac8e964-606f-4010-84a8-7c0ae6ca2133
ms.tgt_platform: multiple
title: Inscription d’un fournisseur d’instances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde8189559b04f2e45ac8357ab47cc17bd253fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923371"
---
# <a name="registering-an-instance-provider"></a>Inscription d’un fournisseur d’instances

Pour créer un [*fournisseur d’instances*](gloss-i.md) WMI, vous devez inscrire l’instance [**\_ \_ Win32Provider**](--win32provider.md) qui représente votre fournisseur à l’aide d’une instance de [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md). En tant qu’objet COM, votre fournisseur doit s’inscrire auprès du système d’exploitation et de WMI. La procédure suivante suppose que vous avez déjà implémenté le processus d’inscription, comme décrit dans [inscription d’un fournisseur](registering-a-provider.md).

La procédure suivante décrit comment inscrire un fournisseur d’instances.

**Pour inscrire un fournisseur d’instances**

1.  Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) qui décrit le fournisseur.
2.  Créez une instance de la classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) qui décrit l’ensemble des fonctionnalités du fournisseur.

    La classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) hérite de nombreuses propriétés de la classe parente [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , qui fournit des valeurs booléennes qui indiquent la prise en charge de fonctionnalités particulières et un tableau de chaînes pour indiquer la prise en charge des requêtes.

    Veillez à baliser la classe avec les qualificateurs [**Dynamic**](standard-wmi-qualifiers.md) et [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) . Le qualificateur indique que WMI doit utiliser un fournisseur **dynamique** pour récupérer les instances de classe. Le qualificateur du **fournisseur** spécifie le nom du fournisseur que WMI doit utiliser.

L’exemple de code suivant décrit comment inscrire une instance [**\_ \_ Win32Provider**](--win32provider.md) et [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
    QuerySupportLevels = { "WQL:UnarySelect" };
};
```

 

 



