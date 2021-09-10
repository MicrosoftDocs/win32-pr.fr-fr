---
title: Définition de la sécurité Process-Wide avec CoInitializeSecurity
description: La fonction CoInitializeSecurity vous permet de contrôler les scénarios de sécurité complexes en définissant la sécurité d’une application par programmation.
ms.assetid: 20b66868-fb9a-489f-97a2-59a8a825c8d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567a6dfaf47dbd278fc248558cd25969c733b24a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363504"
---
# <a name="setting-process-wide-security-with-coinitializesecurity"></a>Définition de la sécurité Process-Wide avec CoInitializeSecurity

La fonction [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) vous permet de contrôler les scénarios de sécurité complexes en définissant la sécurité d’une application par programmation. Cette rubrique décrit les scénarios dans lesquels vous pouvez utiliser **CoInitializeSecurity** et fournit des détails sur la façon dont vous l’utilisez.

Il existe plusieurs raisons pour lesquelles vous pouvez souhaiter utiliser [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) pour définir la sécurité au niveau du processus dans votre programme. Par exemple, bien que vous puissiez définir le niveau d’authentification et les autorisations d’accès de l’application à l’aide de dcomcnfg.exe, le niveau d’emprunt d’identité par défaut de l’ordinateur n’est peut-être pas celui que vous souhaitez pour votre processus. La seule façon de modifier ce paramètre pour votre processus consiste à appeler **CoInitializeSecurity**.

Si vous souhaitez utiliser le fournisseur de sécurité Schannel, vous devez le spécifier en tant que service d’authentification dans un appel à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Un autre scénario courant dans lequel vous pouvez définir la sécurité au niveau du processus par programmation est lorsque vous souhaitez définir la sécurité par défaut pour l’ensemble du processus, mais que vous avez un ou plusieurs objets au sein de ce processus qui exposent des interfaces avec des exigences de sécurité spéciales. Dans ce cas, vous pouvez appeler [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) pour définir la sécurité du processus, ce qui permet à com de gérer la plupart des vérifications de sécurité, et vous pouvez appeler d’autres méthodes pour définir la sécurité pour les objets avec des besoins de sécurité spéciaux. L’appel de ces méthodes et fonctions est décrit dans [définition de la sécurité au niveau du proxy de l’interface](setting-security-at-the-interface-proxy-level.md).

Si votre application a des exigences de sécurité très spécialisées, comme autoriser certains groupes à accéder à différents objets en fonction de l’heure de la journée, vous souhaiterez peut-être gérer l’ensemble de votre sécurité par programme, en veillant à ce que COM n’effectue aucune vérification automatique. Pour ce faire, vous devez appeler [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), en affectant la valeur None au paramètre *DwAuthnLevel* et la **valeur null** au paramètre *pVoid* . Si vous disposez de votre propre package de sécurité, vous devez également l’inscrire dans le paramètre *pAuthnSvc* . Vous pouvez ensuite gérer l’ensemble de votre propre sécurité par programme par le biais d’appels à l’interface de niveau proxy et les fonctions décrites dans [définition de la sécurité au niveau du proxy de l’interface](setting-security-at-the-interface-proxy-level.md).

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) offre un ensemble complet de fonctionnalités. Si vous appelez **CoInitializeSecurity**, les valeurs de Registre sont ignorées et les valeurs d’initialisation de sécurité que vous transmettez à l’appel sont utilisées à la place. Selon le résultat souhaité, le premier paramètre, *pVoid*, peut pointer vers trois types de valeurs différents : un [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , un objet [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) ou un pointeur vers une AppID. dans la plupart des cas, vous utiliserez Windows fonctions pour créer un **\_ descripteur de sécurité** auquel *pVoid* pointera.

Toutefois, *pVoid* peut également pointer vers un objet [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) .

Pour indiquer à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) que vous passez un objet [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) à *pVoid*, vous devez passer la \_ \_ valeur de contrôle d’accès EOAC au paramètre *dwCapabilities* . Dans la mesure où **CoInitializeSecurity** met en cache les résultats des vérifications d’accès, la liste de contrôle d’accès ne doit pas être modifiée après l’appel de **CoInitializeSecurity**.

Un autre type de valeur que vous pouvez passer au paramètre *pVoid* est un pointeur vers un GUID, qui est l’AppID de votre application. Si *pVoid* est un pointeur vers une AppID, vous devez spécifier EOAC \_ AppID dans le paramètre *pCapabilities* afin que la fonction sache quelle valeur attendre dans *pVoid*. Si *pVoid* pointe vers une AppID, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) utilise uniquement le registre pour les valeurs d’authentification et ignore tous les autres paramètres de **CoInitializeSecurity**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de la sécurité Process-Wide](setting-processwide-security.md)
</dt> </dl>

 

 