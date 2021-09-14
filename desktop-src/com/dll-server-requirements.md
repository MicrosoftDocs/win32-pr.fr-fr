---
title: Configuration requise du serveur DLL
description: Alors que la plupart des dll peuvent s’exécuter dans un substitut, certaines dll ne le peuvent pas.
ms.assetid: f89dabe6-f65f-4d90-ad0e-c680d4b08ba5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae82aa44771d398d80169c56976df7b0e209ea6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292779"
---
# <a name="dll-server-requirements"></a>Configuration requise du serveur DLL

Alors que la plupart des dll peuvent s’exécuter dans un substitut, certaines dll ne le peuvent pas.

La DLL doit être correctement comportée si vous souhaitez utiliser le substitut fourni par le système. Par exemple, une DLL qui appelle des méthodes qui inscrivent des rappels à partir du client essaiera d’appeler ces rappels comme si les pointeurs de fonction reçus étaient pour des instructions dans son espace d’adressage, ce qui n’est pas le cas. De même, une DLL qui utilise une variable globale qui s’attend à ce que le client accède ne fonctionnerait pas. En général, les paramètres qui ne peuvent pas être correctement marshalés empêcheront le serveur DLL de s’exécuter en dehors du processus client. Dans de nombreux cas, vous pouvez écrire un substitut personnalisé spécifiquement conçu pour compenser le comportement « incorrect ». (Pour plus d’informations, consultez [écriture d’un substitut personnalisé](writing-a-custom-surrogate.md).)

Si le serveur de DLL utilise des interfaces personnalisées, vous devez vous assurer que le code de marshaling est disponible pour ces interfaces. Par exemple, vous pouvez générer et inscrire une DLL proxy ou fournir et inscrire une bibliothèque de types qui permettrait au serveur de fonctionner correctement lors de son exécution dans un substitut.

Les serveurs DLL sont chargés uniquement dans un processus de substitution s’exécutant dans le contexte de sécurité approprié. Le contexte de sécurité pour le substitut du serveur DLL est déterminé de la même façon que pour les serveurs EXE. Le substitut de serveur DLL s’exécute dans le même contexte de sécurité que le client, à moins qu’une valeur **runas** , qui détermine le contexte de sécurité, soit définie dans la section [AppID](appid-clsid.md) Registry du serveur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Substituts de DLL](dll-surrogates.md)
</dt> </dl>

 

 




