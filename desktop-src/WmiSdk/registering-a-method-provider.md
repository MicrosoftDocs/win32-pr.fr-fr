---
description: Pour créer un fournisseur de méthode WMI, vous devez inscrire l' \_ \_ instance Win32Provider qui représente votre fournisseur à l’aide d’une instance de \_ \_ MethodProviderRegistration.
ms.assetid: 1cfb16ae-8dcf-437d-b779-db2f30bb0d34
ms.tgt_platform: multiple
title: Inscription d’un fournisseur de méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a399f90c6fc6f97e9ada8051055505b43885da3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203729"
---
# <a name="registering-a-method-provider"></a>Inscription d’un fournisseur de méthode

Pour créer un [*fournisseur de méthode*](gloss-m.md) WMI, vous devez inscrire l’instance [**\_ \_ Win32Provider**](--win32provider.md) qui représente votre fournisseur à l’aide d’une instance de [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md). Après avoir créé une instance de [**\_ \_ Win32Provider**](--win32provider.md), vous devez inscrire ce fournisseur auprès de WMI. En tant qu’objet COM, votre fournisseur doit s’inscrire auprès du système d’exploitation et de WMI. La procédure suivante suppose que vous avez déjà implémenté le processus d’inscription, comme décrit dans [inscription d’un fournisseur](registering-a-provider.md).

La procédure suivante décrit comment inscrire un fournisseur de méthodes.

**Pour inscrire un fournisseur de méthode**

1.  Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) qui décrit le fournisseur.

    La classe système [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) hérite de nombreuses propriétés de la classe parente [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) . Toutefois, la seule propriété pertinente pour un fournisseur de méthode est le chemin d’accès de l’objet à l’instance [**\_ \_ Win32Provider**](--win32provider.md) .

2.  Créez une instance de la classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) qui décrit l’ensemble des fonctionnalités du fournisseur.

    Veillez à baliser la classe avec les qualificateurs [**Dynamic**](dynamic-qualifier.md) et [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) . Le qualificateur **dynamique** indique que WMI doit utiliser un fournisseur pour récupérer les instances de classe. Le qualificateur du **fournisseur** spécifie le nom du fournisseur que WMI doit utiliser.

L’exemple de code suivant décrit comment inscrire un fournisseur de méthode.

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "MethProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __MethodProviderRegistration
  {
    Provider = $P;
  };
```

 

 



