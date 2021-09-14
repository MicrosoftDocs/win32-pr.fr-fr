---
description: Constante numérique qui spécifie le nombre maximal de caractères que certains des fournisseurs de services de chiffrement Microsoft utiliseront lors de l’obtention de l’ID utilisateur.
ms.assetid: cc15a166-9a0c-41ce-9cb1-ecdc922565c0
title: MAXUIDLEN (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 199d8e697deba86ffe48d4f76501f2d9d3a6d4e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237492"
---
# <a name="maxuidlen"></a>MAXUIDLEN

MAXUIDLEN est une constante numérique qui spécifie le nombre maximal de caractères que certains des fournisseurs de services de chiffrement Microsoft utiliseront lors de l’obtention de l’ID utilisateur. MAXUIDLEN est défini dans wincrypt. h.



| Constante/valeur                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MAXUIDLEN"></span><span id="maxuidlen"></span><dl> <dt>**MAXUIDLEN**</dt> <dt>64 (0x40)</dt> </dl> | Lorsque le paramètre *pszContainer* de la fonction [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) a la **valeur null**, certains des fournisseurs de services de chiffrement Microsoft utilisent le nom d’ouverture de session de l’utilisateur actuellement connecté comme nom de conteneur de clé. MAXUIDLEN spécifie le nombre maximal de caractères, y compris le caractère **null** de fin, que ces fournisseurs utiliseront pour le nom d’utilisateur.<br/> |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
</dt> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> </dl>

 

 




