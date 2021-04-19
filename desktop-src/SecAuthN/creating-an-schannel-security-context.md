---
description: Explique comment établir un contexte de sécurité qui protège les communications entre un client et un serveur.
ms.assetid: eb1eadb2-14b2-4265-994a-dcea4208e650
title: Création d’un contexte de sécurité Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23e364e6319fbaddb50bffaf59541af9e8f43bfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517073"
---
# <a name="creating-an-schannel-security-context"></a>Création d’un contexte de sécurité Schannel

Pour établir un [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) destiné à protéger les communications entre un client et un serveur, les deux doivent participer au processus d’échange d’informations suivant :

## <a name="client"></a>Client

1.  Le client appelle la fonction [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .
2.  Schannel commence à créer un contexte de sécurité en fonction des règles du protocole de sécurité sélectionné. Le code de retour de la fonction indique si le client doit appeler à nouveau la fonction. [**InitializeSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) peut retourner un jeton qui représente le contexte.
3.  Si un jeton a été retourné, le client l’envoie au serveur.
4.  Lorsque [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) retourne sec \_ E \_ OK, le client est terminé. Si la fonction retourne SEC \_ je \_ continue \_ nécessaire, le client doit attendre que le serveur lui envoie un jeton. Quand le client a le jeton du serveur, il doit appeler à nouveau la [*fonction*](/windows/desktop/SecGloss/c-gly) **InitializeSecurityContext (General)** . (Revenez à l’étape 2.)

## <a name="server"></a>Serveur

1.  Le serveur attend qu’un client envoie un message qui contient un jeton de sécurité. Le serveur transmet le jeton reçu du client à la fonction [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .
2.  Schannel s’appuie sur le contexte de sécurité partiel représenté par le jeton. Schannel retourne un jeton au serveur et un code de retour indiquant si le serveur doit appeler à nouveau la fonction.
3.  Si un jeton a été retourné, le serveur l’envoie au client.
4.  Quand [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) retourne sec \_ E \_ OK, le serveur est terminé. Si la fonction retourne SEC \_ je \_ continue \_ nécessaire, le serveur doit attendre que le client lui envoie un jeton. Lorsque le serveur a le jeton du client, il doit appeler à nouveau la fonction **AcceptSecurityContext (General)** . (Revenez à l’étape 2.)

Si l’une des fonctions retourne une valeur autre que SEC \_ e \_ OK, sec \_ I \_ continue \_ needed ou sec \_ e \_ message Incomplete \_ (voir le paragraphe suivant) une erreur s’est produite. Le client et le serveur doivent appeler la fonction [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) pour supprimer le contexte de sécurité partiellement établi.

Un cas spécial qui peut modifier le traitement du client et du serveur se fait lorsque trop peu ou trop d’informations sont envoyées au client ou au serveur à partir de l’autre partie. Dans le cas d’un trop petit renseignement, les deux fonctions retournent le \_ message E/s \_ incomplet \_ . Pour plus d’informations sur la reconnaissance et la gestion des informations insuffisantes ou excédentaires, consultez [mémoires tampons supplémentaires retournées par Schannel](extra-buffers-returned-by-schannel.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exécution de l’authentification à l’aide de Schannel](performing-authentication-using-schannel.md)
</dt> <dt>

[Mappage des certificats](mapping-certificates.md)
</dt> <dt>

[Validation manuelle des informations d’identification Schannel](manually-validating-schannel-credentials.md)
</dt> </dl>

 

 
