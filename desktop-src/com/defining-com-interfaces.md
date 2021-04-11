---
title: Définition d’interfaces COM
description: Microsoft définit de nombreuses interfaces COM. Dans la plupart des cas, vous pouvez réutiliser ces interfaces génériques. Toutefois, certaines applications ont des exigences spécifiques qui rendent souhaitable ou nécessaire la définition de vos propres interfaces d’objet.
ms.assetid: 8a94bd7d-d101-411c-97de-9e9a46bf9591
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 516c02a2c337b2c76229094b0e42d75b44f65d16
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102401"
---
# <a name="defining-com-interfaces"></a>Définition d’interfaces COM

Microsoft définit de nombreuses interfaces COM. Dans la plupart des cas, vous pouvez réutiliser ces interfaces génériques. Toutefois, certaines applications ont des exigences spécifiques qui rendent souhaitable ou nécessaire la définition de vos propres interfaces d’objet.

Toutes les interfaces COM doivent dériver, directement ou indirectement, de l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Dans cette contrainte, votre interface personnalisée peut prendre en charge presque n’importe quelle méthode ou paramètre, y compris les méthodes asynchrones. Vous pouvez également générer une bibliothèque de types pour vos interfaces personnalisées afin que les clients puissent accéder aux informations sur les méthodes de votre objet au moment de l’exécution. Après avoir défini une interface, la décrire dans Microsoft Interface Definition Language (MIDL), la compiler et l’inscrire, vous pouvez l’utiliser comme n’importe quelle interface générique. Avec COM distribué, les méthodes d’interface sont disponibles à la fois pour les processus distants et pour d’autres processus sur le même ordinateur.

Enfin, la génération d’interfaces COM requiert un environnement de développement qui comprend un compilateur C/C++ et le compilateur Midl.exe.

Les étapes de création d’une interface COM sont les suivantes :

-   Décidez de la façon dont vous souhaitez assurer la prise en charge du marshaling pour votre interface ; que ce soit avec un marshaling piloté par la bibliothèque de types ou avec une DLL proxy/stub. Même les interfaces in-process doivent être marshalées si elles doivent être utilisées dans les limites de cloisonnement. Il est judicieux de créer une prise en charge du marshaling dans chaque interface COM, même si vous ne pensez pas que vous en aurez besoin. Pour plus d’informations, consultez [marshaling d’interface](interface-marshaling.md) .
-   Décrivez l’interface ou les interfaces dans un fichier de définition d’interface (IDL). En outre, vous pouvez spécifier certains aspects locaux de votre interface dans un fichier de configuration d’application (ACF). Si vous utilisez le marshaling piloté par bibliothèque de types, ajoutez une instruction de [**bibliothèque**](/windows/desktop/Midl/library) qui référence les interfaces pour lesquelles vous souhaitez générer des informations de type.
-   Utilisez le compilateur MIDL pour générer un fichier de bibliothèque de types et un fichier d’en-tête, ou des fichiers proxy/stub en langage C, un fichier d’identificateur d’interface, un fichier de données DLL et un fichier d’en-tête. Pour plus d’informations, consultez [compilation MIDL](midl-compilation.md) .
-   Selon la méthode de marshaling choisie, écrivez un fichier de définition de module (DEF), compilez et liez tous les fichiers générés par MIDL dans une DLL de proxy unique, puis inscrivez l’interface dans le registre système ou enregistrez la bibliothèque de types. Pour plus d’informations, consultez [chargement et inscription d’une bibliothèque de types](loading-and-registering-a-type-library.md) et [génération et inscription d’une dll proxy](building-and-registering-a-proxy-dll.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Anatomie d’un fichier IDL](anatomy-of-an-idl-file.md)
</dt> <dt>

[Clients et serveurs COM](com-clients-and-servers.md)
</dt> <dt>

[Règles de conception d’interface](interface-design-rules.md)
</dt> <dt>

[COM (Component Object Model)](the-component-object-model.md)
</dt> </dl>

 

 