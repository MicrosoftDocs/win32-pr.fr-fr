---
description: En plus des classes et des instances, WMI vous permet de modifier une méthode. La principale raison pour laquelle vous souhaitez modifier une méthode est si vous avez modifié l’implémentation d’une méthode dans un fournisseur. Pour plus d’informations, consultez écriture d’un fournisseur de méthodes.
ms.assetid: 239a994f-ecaf-4558-9626-8f5e60dd350c
ms.tgt_platform: multiple
title: Modification d’une méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93009891deec8651599f73f14a73f83bba8ffd4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393328"
---
# <a name="modifying-a-method"></a>Modification d’une méthode

En plus des classes et des instances, WMI vous permet de modifier une méthode. La principale raison pour laquelle vous souhaitez modifier une méthode est si vous avez modifié l’implémentation d’une méthode dans un fournisseur. Pour plus d’informations, consultez [écriture d’un fournisseur de méthodes](writing-a-method-provider.md).

La modification d’une méthode n’est pas une opération qui peut être effectuée dans un script.

La procédure suivante décrit comment modifier une méthode par programme.

**Pour modifier une méthode par programmation**

1.  Récupérez la définition de classe avec un appel à [**IWbemClassObject :: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).

    Les deux paramètres out, *ppInSignature* et *ppOutSignature*, contiennent respectivement la classe in-Parameter et la classe out-Parameter. La valeur de retour est regroupée dans la classe de paramètres de sortie en tant que propriété et doit être nommée **returnValue**.

2.  Récupérez et modifiez les paramètres avec des appels à [**IWbemClassObject :: obten**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)ou [**IWbemClassObject ::D supprim**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).
3.  Placez votre nouvelle version de la méthode dans la classe parente à l’aide d’un appel à [**IWbemClassObject ::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).

 

 



