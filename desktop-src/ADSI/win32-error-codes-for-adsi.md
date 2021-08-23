---
title: Codes d’erreur Win32 pour ADSI
description: Les codes d’erreur Win32 standard sont également utilisés pour retourner des messages d’erreur ADSI.
ms.assetid: 5b7b85c9-ccca-4ea3-8b37-54f6b30a509f
ms.tgt_platform: multiple
keywords:
- Codes d’erreur Win32 pour ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b18539e93504991f244bbba8b41b13e524ff236918145deda73788169cef368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589739"
---
# <a name="win32-error-codes-for-adsi"></a>Codes d’erreur Win32 pour ADSI

Les codes d’erreur Win32 standard sont également utilisés pour retourner des messages d’erreur ADSI. Plus précisément, le fournisseur LDAP ADSI mappe tous les codes d’erreur LDAP aux codes d’erreur Win32. Les valeurs **HRESULT** de ces codes d’erreur sont au format 0x8007XXXX, où les quatre derniers chiffres hexadécimaux, XXXX, correspondent aux valeurs **DWORD** du code d’erreur Win32 approprié. Par exemple, la valeur d’erreur ADSI 0x80072020 donne la valeur d’erreur Win32 0x2020 au format hexadécimal ou 8224 en notation décimale.

Pour convertir la valeur **HRESULT** d’un code d’erreur ADSI, retourné par votre application, en la valeur **DWORD** de l’erreur Win32 correspondante, telle que définie dans les fichiers d’en-tête ci-dessus, utilisez la procédure suivante.

La plupart des codes d’erreur Win32 pour ADSI sont définis dans Winerror. h ou Lmerr. h. Les valeurs d’erreur sont répertoriées sous forme de valeurs décimales dans ces fichiers.

**Pour convertir la valeur **HRESULT** d’un code d’erreur ADSI en la valeur **DWORD** Win32 Error correspondante**

1.  convertit la valeur **HRESULT** en nombre hexadécimal si vous commencez par une valeur décimale, comme vous pouvez l’obtenir à partir d’une application de Visual Basic.
2.  Déposez la partie 0x8007 pour produire le reste.
3.  Convertit le reste en nombre décimal.
4.  Recherchez le reste de la valeur décimale dans Winerror. h.
5.  S’il est introuvable dans Winerror. h, soustraire 2100 du reste décimal et recherchez le résultat dans Lmerr. h.

adsi 2,0 mappe les codes d’erreur LDAP à un ensemble de codes d’erreur Win32 qui est différent de celui utilisé dans ADSI pour les Windows 2000 et DS Client. Les différences sont répertoriées dans :

-   [Codes d’erreur Win32](win32-error-codes.md)
-   [Codes d’erreur Win32 pour ADSI 2,0](win32-error-codes-for-adsi-2-0.md)

 

 




