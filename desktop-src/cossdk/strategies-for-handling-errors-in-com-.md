---
description: Cette rubrique identifie plusieurs stratégies de gestion des erreurs à garder à l’esprit lorsque vous développez des composants pour COM+.
ms.assetid: 1ae5875b-8085-44f2-9071-c2a5d7543ac1
title: Stratégies de gestion des erreurs dans COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca64546683fa45ac8df3bcb47534d8de482798
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127310921"
---
# <a name="strategies-for-handling-errors-in-com"></a>Stratégies de gestion des erreurs dans COM+

Cette rubrique identifie plusieurs stratégies de gestion des erreurs à garder à l’esprit lorsque vous développez des composants pour COM+.

-   **Retourne une valeur HRESULT pour toutes les méthodes dans toutes les interfaces de composant.**  COM+ utilise des valeurs **HRESULT** pour signaler les erreurs lors de l’exécution d’appels de fonction ou d’appels de méthode d’interface. Un **HRESULT** indique si une méthode a réussi ou échoué et identifie la fonction associée à l’erreur, telle que RPC, Win32 ou ITF pour les erreurs spécifiques à l’interface. En outre, les API système fournissent une recherche d’une valeur **HRESULT** à une chaîne qui décrit la condition d’erreur. L’utilisation de méthodes qui retournent des valeurs **HRESULT** est fondamentale pour les composants bien écrits et est essentielle au processus de débogage. Microsoft Visual Basic définit automatiquement chaque méthode avec un **HRESULT** comme retour. dans Microsoft Visual C++, vous devez retourner explicitement un **HRESULT**. Pour plus d’informations sur les valeurs HRESULT, consultez [structure des codes d’erreur com](/windows/desktop/com/structure-of-com-error-codes).
-   **Lancez l’objet de collection ErrorInfo en fonction de ce que fournit votre outil de développement.** Les objets de collection [**errorInfo**](errorinfo.md) sont souvent appelés exceptions com, car ils permettent à un objet de passer (ou d’envoyer) des informations d’erreur riches à son appelant, même au-delà des limites de cloisonnement. La valeur de cet objet d’erreur générique est qu’il complète un HRESULT, en étendant le type d’informations d’erreur que vous pouvez retourner à un appelant. Chaque objet de collection **errorInfo** retourne une description contextuelle, la source de l’erreur et l’identificateur d’interface de la méthode à l’origine de l’erreur. Vous pouvez également inclure des pointeurs vers une entrée dans un fichier d’aide. Automation fournit trois interfaces pour gérer l’objet d’erreur. Votre composant doit implémenter l’interface d’automatisation **ISupportErrorInfo** pour annoncer sa prise en charge pour la collection **errorInfo** . Lorsqu’une erreur se produit, le composant utilise l’interface d’automatisation **ICreateErrorInfo** pour initialiser un objet d’erreur. Une fois que l’appelant a inspecté la valeur HRESULT et a détecté que l’appel de la méthode a échoué, il interroge l’objet pour voir s’il prend en charge la collection **errorInfo** . Si c’est le cas, l’appelant utilise l’interface d’automatisation **IErrorInfo** pour récupérer les informations sur l’erreur. Visual Basic programmeurs ont un accès facile à l’objet de collection **ErrorInfo** , qui est exposé via l’objet Err. Vous pouvez déclencher des erreurs avec la fonction Err Raise et intercepter les erreurs avec l’instruction **On Error** . la couche d’exécution Visual Basic prend en charge le mappage pour vous. Si vous utilisez la prise en charge du compilateur COM Visual C++, vous pouvez utiliser la \_ \_ \_ classe d’erreur com Raise pour signaler une erreur et la \_ \_ classe d’erreur com pour récupérer les informations d’erreur. COM+ ne propage pas les exceptions C++ traditionnelles en tant qu’informations **IErrorInfo** étendues. Pour plus d’informations sur l’objet de collection **errorInfo** , consultez « Gestion des erreurs » dans le Guide d’automatisation.
    > [!Note]  
    > COM requiert que tous les objets de collection [**errorInfo**](errorinfo.md) soient marshalés par valeur, ce qui implique que les composants qui implémentent l’interface d’automatisation **IErrorInfo** doivent également implémenter et prendre en charge l’interface [**IMarshal**](/windows/desktop/api/objidl/nn-objidl-imarshal) . L’implémentation de l’interface **IMarshal** doit prendre en charge Marshal by value pour le composant.

     

-   **Utilisez des transactions pour gérer les échecs de ressources partagées.** Les transactions automatiques peuvent réduire considérablement la quantité de code de gestion des erreurs que vous devez écrire lors de l’utilisation de gestionnaires de ressources gérés par État. Toutefois, les transactions n’éliminent pas complètement la nécessité de gérer les erreurs. Vous devez toujours retourner des codes d’erreur à partir de vos méthodes d’interface et vérifier ces codes d’erreur dans l’appelant pour éviter tout travail inutile pour une transaction vouée. Pour plus d’informations sur la combinaison de la gestion des erreurs avec le traitement des transactions, consultez [accélération des transactions en avertissant l’objet racine](speeding-transactions-by-notifying-the-root-object.md).
-   **Déclencher des erreurs explicitement.** Évitez de laisser les informations d’erreur laisser un objet, sauf si l’objet déclenche explicitement l’erreur. Interceptez toutes les erreurs générées par l’outil et gérez-les dans le code de votre composant. Au minimum, incluez un gestionnaire standard pour signaler les erreurs inattendues de manière cohérente.
-   **Utilisez la \_ plage d’erreurs ITF pour signaler des erreurs spécifiques à l’interface.** Les erreurs spécifiques à l’interface doivent se trouver dans la \_ plage d’erreurs ITF, entre 0x0200 et 0xFFFF. vous pouvez définir un code d’erreur personnalisé dans Visual Basic en tant que décalage à partir de vbObjectError. Utilisez la \_ macro make HRESULT en C++ pour introduire un code d’erreur spécifique à l’interface, comme indiqué dans l’exemple suivant :

    ``` syntax
    const HRESULT ERROR_NUMBER = MAKE_HRESULT (SEVERITY_ERROR, FACILITY_ITF, 10);
    ```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Isolation des erreurs et stratégie FailFast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Recherche de la source d’une erreur](finding-the-source-of-an-error.md)
</dt> <dt>

[Modification des valeurs de retour par COM+](how-com--modifies-return-values.md)
</dt> <dt>

[Interprétation des codes d’erreur](interpreting-error-codes.md)
</dt> <dt>

[Dépannage](troubleshooting.md)
</dt> </dl>

 

 
