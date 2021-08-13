---
title: Erreurs courantes (ADSI)
description: Toutes les erreurs spécifiques à ADSI ont une forme hexadécimale de 80005xxx. Les codes d’erreur les plus courants sont décrits dans le tableau suivant.
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efcbbbce67d9928c9ecda3840f34a1cbf6faae79ca4d9fe72830a5b57881177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692193"
---
# <a name="common-errors-adsi"></a>Erreurs courantes (ADSI)

Toutes les erreurs spécifiques à ADSI ont une forme hexadécimale de 80005xxx. Les codes d’erreur les plus courants sont décrits dans le tableau suivant.



| Code d’erreur hexadécimal ADSI | Description                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 80005000<br/> | Un chemin d’accès ADSI non valide a été passé. Cette erreur est due au passage d’un ADsPath mal formé à **GetObject** lors de la liaison à un objet.<br/> |
| 8000500D<br/> | La propriété ADSI est introuvable dans le cache de propriétés.<br/>                                                                                 |
| 8000500E<br/> | L’objet ADSI existe. Si vous tentez de créer un objet ADSI portant le même nom qu’un objet ADSI existant, cette erreur se produit.<br/>    |



 

Pour obtenir la liste complète des codes d’erreur ADSI, consultez [codes d’erreur ADSI génériques](generic-adsi-error-codes.md).

## <a name="com-errors"></a>Erreurs COM

Étant donné que l’interface ADSI est composée d’objets COM, elle renverra des codes d’erreur COM standard. Le tableau suivant répertorie les codes d’erreur COM les plus couramment rencontrés dans la programmation ADSI.



| Code d’erreur hexadécimal COM  | Description                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| 80004005<br/> | Erreur non spécifiée. La cause de l’échec de l’objet COM est indéterminée par ADSI. <br/>                                  |
| 800041E4<br/> | Objet introuvable. Cette erreur se produit principalement en raison d’une mauvaise orthographe de la chaîne ADsPath lors de la liaison à un objet.<br/> |



 

Consultez [codes d’erreur com génériques](generic-com-error-codes.md) pour obtenir d’autres exemples d’erreurs com susceptibles de se produire dans la programmation ADSI.

## <a name="win32-errors"></a>Erreurs Win32

Tout code d’erreur de forme hexadécimale 8007xxxx est un code d’erreur Win32 standard. si vous convertissez les quatre derniers chiffres du format hexadécimal au format décimal, vous pouvez accéder à l’erreur à partir de la ligne de commande Windows 2000 :

**net helpmsg <number>**

Dans la ligne de commande ci-dessus, « &lt; Number &gt; » est le nombre décimal obtenu en convertissant les quatre derniers chiffres du code d’erreur au format hexadécimal. Cette ligne de commande fournit une description plus utile de l’erreur Win32, qui peut vous aider à déboguer votre script.

 

 





