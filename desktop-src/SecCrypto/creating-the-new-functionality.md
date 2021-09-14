---
description: Les fonctions suivantes font partie des fonctions CryptoAPI qui peuvent être étendues.
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: Création de la nouvelle fonctionnalité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d660c14e99247c7d17f57100858b104d1cbcc9ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123230"
---
# <a name="creating-the-new-functionality"></a>Création de la nouvelle fonctionnalité

Les fonctions suivantes font partie des fonctions CryptoAPI qui peuvent être étendues.



| CryptoAPI, fonction                                   | Nom de la fonction OID define                         | Chaîne de nom de la fonction OID  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | chiffrer l' \_ \_ \_ objet \_ Func OID encode<br/>     | "CryptDllEncodeObject"    |
| [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | CRYPT \_ OID \_ décoder l' \_ objet \_ Func<br/>     | "CryptDllDecodeObject"    |
| [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | chiffrer le \_ \_ magasin Open OID Open \_ Store \_ \_<br/>  | "CertDllOpenStoreProv"    |
| [**CertVerifyCTLUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | CRYPT \_ OID \_ - \_ vérifier \_ l’utilisation de la liste CTL \_<br/> | "CertDllVerifyCTLUsage"   |
| [**CertVerifyRevocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | chiffrer la vérification de la \_ \_ \_ révocation des OID \_<br/> | "CertDllVerifyRevocation" |



 

En mode d’utilisation normale avec un OID et un type d’encodage existants, le code de la fonction CryptoAPI, lui-même, est utilisé. Si l’une de ces fonctions est appelée avec un OID et que le type d’encodage n’a pas été conçu pour gérer le code de la fonction CryptoAPI, une nouvelle fonction, contenant les nouvelles fonctionnalités, doit être créée dans une DLL. Cette DLL doit être inscrite dans le registre ou installée en mémoire.

Lorsque l’une des fonctions répertoriées est appelée avec l’OID et le type d’encodage récemment désignés, le code de la nouvelle DLL est utilisé au lieu du code fourni dans le cadre de la fonction CryptoAPI.

Le nom de la fonction nouvellement développée peut être le nom répertorié sous « OID Function name string » dans le tableau précédent, ou un autre nom peut être donné lorsque le nouveau code de la fonction est inscrit.

La nouvelle fonction doit utiliser un prototype approprié. Dans tous les cas, à l’exception de [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), ce prototype est le même que la fonction CryptoAPI qui appelle la nouvelle fonction. Dans le cas de **CertOpenStore** , le prototype est le suivant.


```C++
#include <windows.h>

BOOL WINAPI CertDllOpenStoreProv(
  IN LPCSTR lpszStoreProvider,
  IN DWORD dwEncodingType,
  IN HCRYPTPROV hCryptProv,
  IN DWORD dwFlags,
  IN const void *pvPara,
  IN HCERTSTORE hCertStore,
  IN OUT PCERT_STORE_PROV_INFO pStoreProvInfo
);
```



> [!Note]  
> Si les prototypes ne correspondent pas, la pile système est endommagée.

 

En plus de fournir le code de la nouvelle fonction dans une DLL, l’extension de la fonctionnalité de [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) ou [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) nécessite la définition d’une définition de type pour que la nouvelle structure de données C soit placée dans un fichier d’en-tête inclus lorsque le programme de l’utilisateur est compilé.

 

 




