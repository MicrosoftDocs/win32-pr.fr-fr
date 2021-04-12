---
description: Client-Side la configuration requise pour l’emprunt d’identité
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: Client-Side la configuration requise pour l’emprunt d’identité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c3c188f3c03e46a0e6e414efc66c5fdd2366d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317941"
---
# <a name="client-side-requirements-for-impersonation"></a>Client-Side la configuration requise pour l’emprunt d’identité

Les deux paramètres suivants peuvent être spécifiés par rapport à l’emprunt d’identité côté client :

-   Le niveau d’emprunt d’identité, qui indique la volonté du client de faire en sorte que le serveur utilise son identité.
-   Paramètre du service Active Directory par le biais duquel le compte client peut être marqué « le compte est sensible et ne peut pas être délégué », ce qui désactive la délégation.

Le niveau d’emprunt d’identité peut être défini de différentes façons. Si le client n’indique pas un niveau d’emprunt d’identité, la valeur par défaut à l’échelle de l’ordinateur est utilisée par COM. La valeur par défaut à l’ensemble de l’ordinateur peut être définie à l’aide de l’outil d’administration Services de composants ou Dcomcnfg.exe. Le client peut également indiquer un niveau d’emprunt d’identité préféré de manière administrative avec Dcomcnfg.exe.

Le client peut indiquer le niveau d’emprunt d’identité par programmation, à l’aide de [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), équivalent à [**IClientSecurity :: SetBlanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), qui peut être appelé aussi souvent que nécessaire, ou [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), qui peut être appelé une fois par processus.

Si le client indique l’emprunt d’identité au niveau du délégué (l’autorité la plus étendue qu’il peut accorder au serveur), le client doit s’exécuter sous une identité correctement configurée dans le service Active Directory pour permettre la délégation de son identité.

Pour plus d’informations sur les niveaux d’emprunt d’identité et la configuration requise pour le fonctionnement de la délégation, consultez [délégation et emprunt d’identité](/windows/desktop/com/delegation-and-impersonation).

Les applications COM+ peuvent toujours agir comme des clients, bien sûr. Lorsque l’application COM+ fait un appel à une autre application ou ressource, elle exprime un niveau d’emprunt d’identité. Pour les applications serveur COM+, vous pouvez définir un niveau d’emprunt d’identité de manière administrative. Les applications de bibliothèque COM+ ne peuvent pas définir leur propre niveau d’emprunt d’identité ; ils utilisent à la place celui du processus hôte. Pour savoir comment définir l’emprunt d’identité pour une application COM+, consultez [définition d’un niveau d’emprunt d’identité](setting-an-impersonation-level.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Emprunt d’identité et délégation du client](client-impersonation-and-delegation.md)
</dt> <dt>

[Masquer](cloaking.md)
</dt> <dt>

[Exigences côté serveur pour l’emprunt d’identité](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
