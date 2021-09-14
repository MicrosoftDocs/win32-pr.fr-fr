---
title: Corps de l’interface IDL
description: Le corps de l’interface IDL contient les types de données utilisés dans les appels de procédure distante et les prototypes de fonction pour les procédures distantes.
ms.assetid: b07524a7-b27e-4ea2-ae34-068c07d9a444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565cbe6493bd865030b77b5e9ef6275b444ca451
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416577"
---
# <a name="the-idl-interface-body"></a>Corps de l’interface IDL

Le corps de l’interface IDL contient les types de données utilisés dans les appels de procédure distante et les prototypes de fonction pour les procédures distantes. Le corps de l’interface peut également contenir des importations, des pragmas, des déclarations de constantes et des déclarations de type. En mode Microsoft-extensions, le compilateur MIDL autorise également les déclarations implicites sous la forme de définitions de variables.

L’exemple suivant montre un fichier IDL contenant la définition d’une interface. Le corps de la définition d’interface, qui se produit entre les accolades, contient la définition d’une constante (**bufsize**), un type **( \_ \_ type de handle PCONTEXT**) et certaines procédures distantes (**RemoteOpen**, **RemoteRead**, **RemoteClose** et **Shutdown**).

``` syntax
[ 
  uuid (ba209999-0c6c-11d2-97cf-00c04f8eea45), 
  version(1.0), 
  pointer_default(unique) 
] 
interface cxhndl 
{ 
 
  const short BUFSIZE = 1024;  
 
  typedef [context_handle] void *PCONTEXT_HANDLE_TYPE; 
 
  short RemoteOpen( 
      [out] PCONTEXT_HANDLE_TYPE *pphContext, 
      [in, string] unsigned char *pszFile 
  ); 
 
   short RemoteRead( 
      [in]  PCONTEXT_HANDLE_TYPE phContext, 
      [out] unsigned char achBuf[BUFSIZE], 
      [out] short *pcbBuf 
  ); 
 
  short RemoteClose( [in, out] PCONTEXT_HANDLE_TYPE *pphContext ); 
 
  void Shutdown(void); 
 
}
```

Pour plus d’informations, consultez [Référence du langage MIDL](/windows/desktop/Midl/midl-language-reference).

 

 