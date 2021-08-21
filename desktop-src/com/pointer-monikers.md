---
title: Monikers de pointeur
description: Un moniker de pointeur identifie un objet qui ne peut exister qu’en état actif ou en cours d’exécution. Cela diffère des autres classes de monikers, qui identifient les objets qui peuvent exister dans l’état passif ou actif.
ms.assetid: 9895f03d-7110-41c1-a934-87010f9ad380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcdf96497751b3f777c292c56d35b2c04432da84b352e20c4dd8b0917dedb16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047897"
---
# <a name="pointer-monikers"></a>Monikers de pointeur

Un *moniker de pointeur* identifie un objet qui ne peut exister qu’en état actif ou en cours d’exécution. Cela diffère des autres classes de monikers, qui identifient les objets qui peuvent exister dans l’état passif ou actif.

Supposons, par exemple, qu’une application possède un objet qui n’a pas de représentation persistante. Normalement, si un client de votre application a besoin d’accéder à cet objet, vous pouvez simplement transmettre au client un pointeur vers l’objet. Toutefois, supposons que votre client attende un moniker. L’objet ne peut pas être identifié par un moniker de fichier, car il n’est pas stocké dans un fichier, ni avec un moniker d’élément, car il n’est pas contenu dans un autre objet.

Au lieu de cela, votre application peut créer un moniker de pointeur, qui est un moniker qui contient simplement un pointeur en interne et le transmet au client. Le client peut traiter ce moniker comme tout autre. Toutefois, lorsque le client appelle [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) sur le moniker du pointeur, le code du moniker ne vérifie pas la table ROT (Running Object Table) ou ne charge rien à partir du stockage. Au lieu de cela, le code du moniker appelle simplement [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le pointeur stocké à l’intérieur du moniker.

Les monikers de pointeur autorisent les objets qui existent uniquement dans l’état actif ou en cours d’exécution pour participer aux opérations de moniker et sont utilisés par les clients moniker. Une différence importante entre les monikers de pointeur et d’autres classes de monikers est que les monikers de pointeur ne peuvent pas être enregistrés dans un stockage persistant. Si vous le faites, l’appel de la méthode [**IMoniker :: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) retourne une erreur. Cela signifie que les monikers de pointeur sont utiles uniquement dans des situations particulières. Vous pouvez utiliser la fonction [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) si vous devez utiliser un moniker de pointeur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Anti-monikers](anti-monikers.md)
</dt> <dt>

[Monikers de classe](class-monikers.md)
</dt> <dt>

[Monikers composites](composite-monikers.md)
</dt> <dt>

[Monikers de fichiers](file-monikers.md)
</dt> <dt>

[Monikers d’élément](item-monikers.md)
</dt> </dl>

 

 




