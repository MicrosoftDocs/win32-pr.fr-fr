---
title: Modèle de Data-Pull et modèle de Data-Push
description: Modèle de Data-Pull et modèle de Data-Push
ms.assetid: ba0e8532-9c7b-4e15-9c27-8205d738fc4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f6607e9b466c439859a99b857e7ce3fe6d8acd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104383015"
---
# <a name="data-pull-model-and-data-push-model"></a>Modèle de Data-Pull et modèle de Data-Push

Un client d’un moniker asynchrone peut choisir entre un modèle d’extraction de données et d’envoi de données pour conduire une opération asynchrone [**IMoniker :: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) et recevoir des notifications asynchrones. Dans le modèle d’extraction de données, le client pilote l’opération de liaison et le moniker fournit des données au client uniquement lorsqu’il est lu. En d’autres termes, après le premier appel à [**IBindStatusCallback :: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), le moniker ne fournit aucune donnée au client, sauf si le client a consommé toutes les données qui sont déjà disponibles.

Étant donné que les données sont téléchargées uniquement lorsqu’elles sont demandées, les clients qui choisissent le modèle d’extraction de données doivent veiller à lire ces données en temps voulu. Dans le cas des téléchargements Internet avec [monikers d’URL](url-monikers.md), l’opération de liaison peut échouer si un client attend trop de temps avant de demander des données supplémentaires.

Dans le modèle de transmission de données, le moniker pilote l’opération de liaison asynchrone et notifie en continu au client chaque fois que de nouvelles données sont disponibles. Le client peut choisir de lire ou non les données à tout moment pendant l’opération de liaison, mais le moniker va entraîner l’achèvement de l’opération de liaison, quelle que soit la valeur de l’opération de liaison.

En outre, vous devez penser à suivre les règles COM pour l’allocation de mémoire lors de l’utilisation de monikers asynchrones, en particulier les éléments suivants :

-   Chaque fois qu’un appel de fonction ou d’interface COM retourne une mémoire tampon (String ou other) à son client, le client est responsable de la libération de la mémoire en appelant [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).
-   Chaque fois qu’une fonction ou une interface COM requiert une mémoire tampon de son client, le client doit allouer ce tampon à l’aide de [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) et l’appelé doit le libérer.

Veillez à respecter ces règles lors de l’allocation de chaînes ou de mémoires tampons transmises à des monikers asynchrones, et n’oubliez pas de libérer de la mémoire retournée par les monikers asynchrones. Pour plus d’informations, consultez Gestion de l' [allocation de mémoire](the-com-library.md) et des rubriques connexes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Monikers asynchrones](asynchronous-monikers.md)
</dt> </dl>

 

 