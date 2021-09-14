---
description: Les énumérations ont tendance à utiliser une quantité importante de ressources système.
ms.assetid: 4163e6c2-4ee3-4906-b297-618509666c90
ms.tgt_platform: multiple
title: Amélioration des performances d’énumération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2554e9e1df2f2ece58f5703d6099d84acbe01c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915763"
---
# <a name="improving-enumeration-performance"></a>Amélioration des performances d’énumération

Les énumérations ont tendance à utiliser une quantité importante de ressources système. Par conséquent, vous devez essayer d’optimiser le processus d’énumération WMI si vous envisagez d’effectuer des énumérations sur un grand groupe. Les scripts peuvent également utiliser une requête pour éviter une dégradation des performances dans les opérations « for each.... Next » avec un grand ensemble. Pour plus d’informations, consultez [interrogation de WMI](querying-wmi.md).

La procédure suivante décrit comment améliorer les performances de l’énumération.

**Pour améliorer les performances de l’énumération**

1.  Définissez le paramètre *lFlags* pour autoriser le retour semi-synchrone des données avec un énumérateur qui ignore chaque élément de WMI lorsqu’il est remis. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

    L’exemple de code C++ suivant montre comment utiliser l' **indicateur WBEM pour \_ \_ retourner \_** les indicateurs de transfert immédiat et de l' **\_ indicateur WBEM \_ Forward \_ uniquement** .

    `WBEM_FLAG_RETURN_IMMEDIATE | WBEM_FLAG_FORWARD_ONLY`

    dans VBScript ou Visual Basic, utilisez les indicateurs de script **WbemFlagReturnImmediately** et **WbemFlagForwardOnly** à partir de [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum). La valeur combinée de ces indicateurs est décimale 48.

    Les indicateurs de script et de paramètre provoquent le comportement suivant :

    -   L' **\_ indicateur WBEM \_ retourne \_** le comportement semi-synchrone ou **wbemFlagReturnImmediately** des demandes d’indicateur. L’appel pour créer l’énumérateur est retourné immédiatement. Vous pouvez ensuite commencer à parcourir le jeu d’objets que vous recevez.
    -   L’indicateur de progression de l' **\_ indicateur WBEM \_ \_ uniquement** ou **wbemFlagForwardOnly** demande un énumérateur que vous ne pouvez pas rembobiner. Autrement dit, WMI peut libérer un objet une fois que vous avez affiché l’objet.

    Dans les situations où l’énumération est volumineuse et l’application est très rapide, l’utilisation d’énumérateurs avant uniquement avec le traitement semi-synchrone permet à WMI de conserver beaucoup moins d’objets, ce qui augmente considérablement le temps de réponse et les performances de la mémoire.

    L’exemple de code VBScript suivant montre comment effectuer un appel à l’aide des indicateurs **wbemFlagReturnImmediately** et **wbemFlagForwardOnly** combinés pour obtenir une collection d’événements à partir d’un journal des événements.

    ```VB
    Set Events = GetObject("winmgmts:").ExecQuery _
         ("SELECT * FROM Win32_NTLogEvent " _
          & "WHERE Logfile = 'System'",,48)
    ```

    

2.  Dans la mesure du possible, évitez d’utiliser [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) en C++ ou [**SWbemServices. InstancesOf**](swbemservices-instancesof.md), et utilisez à la place **ExecQuery**.

    La méthode **ExecQuery** interroge WMI à l’aide des technologies de base de données, tandis que [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) ou [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) énumère les objets WMI. Plus précisément, **ExecQuery** peut demander des sous-ensembles spécifiques de données que les méthodes d’énumération ne peuvent pas.

    Étant donné que certains fournisseurs n’ont pas de fonctionnalités d’interrogation, WMI fournit une fonctionnalité « filtre de publication » qui permet à WMI d’ignorer les instances qui ne répondent pas aux spécifications de la requête. Le fait qu’un fournisseur particulier tire parti de cette fonctionnalité dépend de l’auteur du fournisseur.

3.  Faites des essais avec différentes requêtes pour déterminer ce qui offre les meilleures performances.

    Par exemple, WMI traite rarement efficacement les requêtes avec des clauses **Where** de la forme Prop1 < « x ». En revanche, WMI traite normalement les requêtes de la forme KeyProp1 = "x" efficacement.

Pour plus d’informations, consultez la page [énumération de WMI](enumerating-wmi.md).

 

 



