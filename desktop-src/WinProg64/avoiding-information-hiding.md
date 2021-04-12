---
title: Éviter le masquage des informations
description: Parfois, les programmes masquent les informations délibérément ou par inadvertance à partir du moteur de marshaling RPC.
ms.assetid: 016b9221-092d-4c25-a396-4f41dcdfb3cf
keywords:
- compatibilité descendante avec la programmation Windows 64 bits
- problèmes de compatibilité 64-programmation Windows bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4b9e4ba7ed5165378beb93005243af03f9e469
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382218"
---
# <a name="avoiding-information-hiding"></a>Éviter le masquage des informations

Parfois, les programmes masquent les informations délibérément ou par inadvertance à partir du moteur de marshaling RPC. Voici quelques exemples :

-   Envoi d’une structure de données sous la forme d’un bloc d’octets non différencié
-   Tirer parti des performances à l’aide d’un effet secondaire d’une méthode pour canaliser des données supplémentaires sur le réseau
-   Tentative de déguisement d’un handle en le transmettant en tant que **DWORD** ou **ULong**

Il est presque garanti que ces techniques introduisent des problèmes de compatibilité avant de porter votre application sur Windows 64 bits.

Au lieu d’envoyer un contexte de serveur en tant que **valeur DWORD** dans un appel de procédure distante standard, utilisez un handle de contexte pour fournir un handle opaque à un contexte de serveur détenu pour le compte d’un client. Les contextes sont identifiés par des GUID définis par le runtime d’exécution RPC lorsqu’un serveur crée un handle de contexte pour un client. Aucun pointeur n’est utilisé sur le câble et l’opération est complètement transparente sur les limites de 32 ou 64 bits. Pour plus d’informations sur l’utilisation des handles de contexte, consultez [Handles de contexte](/windows/desktop/Rpc/context-handles).

Les interfaces DCOM ne peuvent pas utiliser de handles de contexte, car COM fournit sa propre gestion de contexte. Au lieu de créer un handle de contexte, vous pouvez passer un pointeur d’interface à l’objet COM. Vous pouvez ensuite appeler les méthodes directement par le biais du pointeur d’interface ou placer le pointeur à l’intérieur d’autres appels. Pour libérer l’objet serveur, le client appelle la méthode **Release** de l’interface par le biais du pointeur d’interface.

Là encore, il peut arriver que vous ne pouvez pas modifier la conception originale du code que vous portez. S’il n’existe aucun moyen d’éviter d’envoyer un pointeur sur le câble en tant que **valeur DWORD**, vous devez implémenter une forme de mappage côté serveur entre les valeurs **DWORD** et les pointeurs. Pour ce faire, vous pouvez modifier les pointeurs de l’application côté client en types de pointeurs de précision, tels que **ULong \_ ptr** ou **DWORD \_ ptr**. Utilisez ensuite l' \[ [**appel MIDL \_ en tant qu'**](/windows/desktop/Midl/call-as) \] attribut pour placer les pointeurs sur le câble en tant que valeurs **DWORD** . Le wrapper côté client ne doit passer les arguments qu’en même temps. Le wrapper côté serveur gère le mappage entre les deux types. De la même façon, vous pouvez utiliser l’attribut \[ [**transmettre \_ en tant que**](/windows/desktop/Midl/transmit-as) \] ou l' \[ attribut [**représenter \_ en tant que**](/windows/desktop/Midl/represent-as) \] pour convertir vos données dans un format à compatibilité descendante pour la représentation filaire.

Si la compatibilité de la transmission descendante n’est pas un problème ou si le handle n’est pas utilisé pour les appels distants et si vous êtes sûr que les appels distants entre les processus 32 et 64 bits ne se produiront jamais, vous pouvez redéfinir un argument en tant que **ULONG64**. Si nécessaire, vous pouvez modifier l’application 32 bits pour transmettre un **DWORD** à l’utilisateur. Vous pouvez également créer des stubs distincts à partir de fichiers IDL distincts pour chaque plateforme à l’aide d’un **DWORD** sur Windows 32 bits et un **ULONG64** sur Windows 64 bits.

 

 