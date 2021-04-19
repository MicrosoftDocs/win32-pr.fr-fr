---
title: Choix des options de QOS de sécurité
description: Les options QOS de sécurité sont transmises dans le cadre du paramètre SecurityQOS donné à la fonction RpcBindingSetAuthInfoEx. Utilisez les meilleures pratiques suivantes.
ms.assetid: 43befe3d-079a-4389-a1ff-6bda90935769
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c286b516438eae78117ef8d73939c3b4bed396d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510090"
---
# <a name="choosing-security-qos-options"></a>Choix des options de QOS de sécurité

Les options QOS de sécurité sont transmises dans le cadre du paramètre *SecurityQOS* donné à la fonction [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) . Utilisez les meilleures pratiques suivantes.

## <a name="use-mutual-authentication"></a>Utiliser l’authentification mutuelle

La véritable authentification mutuelle est disponible uniquement pour certains fournisseurs de sécurité : Negotiate (quand elle négocie Kerberos), Kerberos et Schannel. NTLM ne prend pas en charge l’authentification mutuelle. L’authentification mutuelle requiert qu’un nom principal de serveur bien formé soit fourni. De nombreux développeurs utilisent la pratique de sécurité défectueuse suivante : le serveur est appelé pour demander son nom principal ([**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)), puis il demande une authentification mutuelle à l’aide de ce nom principal. Cette approche rompt l’idée entière de l’authentification mutuelle. l’idée de l’authentification mutuelle est que seuls certains serveurs sont appelés, car ils sont approuvés pour analyser et gérer vos données. À l’aide de la pratique de sécurité défectueuse qui vient d’être décrite, les développeurs donnent leurs données à toute personne suffisamment intelligente pour retourner leur nom.

Par exemple, si le logiciel client doit appeler uniquement un serveur s’exécutant sous Joe, Pete ou les comptes d’Alice, la fonction [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname) doit être appelée et le nom renvoyé doit être vérifié. S’il s’agit de Joe, Pete ou Alice, l’authentification mutuelle doit être demandée à l’aide de son nom principal de serveur. Cela permet de s’assurer que les deux moitiés de la conversation sont dirigées vers le même principal.

Si le logiciel client doit appeler un service s’exécutant uniquement sous le compte de Jean, rédigez directement le nom principal du serveur de Joe et effectuez l’appel. Si le serveur n’est pas Joe, l’appel échoue tout simplement.

De nombreuses fois, les services s’exécutent en tant que services système Windows, ce qui signifie qu’ils s’exécutent sous le compte de l’ordinateur. L’authentification mutuelle et la création d’un nom principal de serveur sont toujours recommandées.

## <a name="use-the-lowest-impersonationtype-that-allows-the-call-to-go-through"></a>Utiliser le ImpersonationType le plus bas qui autorise l’appel à passer

Cette meilleure pratique est assez explicite. Même si l’authentification mutuelle est utilisée, ne donnez pas au serveur plus de droits que nécessaire. un serveur légitime a peut-être été compromis, et même si les données que vous envoyez tombent dans de mauvaises mains, au moins le serveur ne pourra pas accéder à d’autres données sur le réseau à votre place. Certains serveurs rejetteront un appel qui ne dispose pas d’informations suffisantes pour déterminer et éventuellement emprunter l’identité de l’appelant. Sachez également que certaines séquences de protocole prennent en charge la sécurité au niveau du transport ([**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) et [**Ncalrpc**](/windows/desktop/Midl/ncalrpc)). Dans ce cas, le serveur peut toujours emprunter l’identité si vous spécifiez un niveau d’emprunt d’identité suffisamment élevé par le biais du paramètre *NetworkOptions* lorsque vous créez le handle de liaison.

Enfin, certains fournisseurs de sécurité ou transports peuvent enbosser de manière transparente ImpersonationType à un niveau supérieur à celui spécifié. Lors du développement d’un programme, assurez-vous d’effectuer des appels avec le ImpersonationType prévu et vérifiez si vous obtenez une ImpersonationType supérieure sur le serveur.

 

 