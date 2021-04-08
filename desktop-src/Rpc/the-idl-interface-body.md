---
title: Corps de l’interface IDL
description: Le corps de l’interface IDL contient les types de données utilisés dans les appels de procédure distante et les prototypes de fonction pour les procédures distantes.
ms.assetid: b07524a7-b27e-4ea2-ae34-068c07d9a444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565cbe6493bd865030b77b5e9ef6275b444ca451
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728669"
---
# <a name="the-idl-interface-body"></a><span data-ttu-id="a8edd-103">Corps de l’interface IDL</span><span class="sxs-lookup"><span data-stu-id="a8edd-103">The IDL Interface Body</span></span>

<span data-ttu-id="a8edd-104">Le corps de l’interface IDL contient les types de données utilisés dans les appels de procédure distante et les prototypes de fonction pour les procédures distantes.</span><span class="sxs-lookup"><span data-stu-id="a8edd-104">The IDL interface body contains data types used in remote procedure calls and the function prototypes for the remote procedures.</span></span> <span data-ttu-id="a8edd-105">Le corps de l’interface peut également contenir des importations, des pragmas, des déclarations de constantes et des déclarations de type.</span><span class="sxs-lookup"><span data-stu-id="a8edd-105">The interface body can also contain imports, pragmas, constant declarations, and type declarations.</span></span> <span data-ttu-id="a8edd-106">En mode Microsoft-extensions, le compilateur MIDL autorise également les déclarations implicites sous la forme de définitions de variables.</span><span class="sxs-lookup"><span data-stu-id="a8edd-106">In Microsoft-extensions mode, the MIDL compiler also allows implicit declarations in the form of variable definitions.</span></span>

<span data-ttu-id="a8edd-107">L’exemple suivant montre un fichier IDL contenant la définition d’une interface.</span><span class="sxs-lookup"><span data-stu-id="a8edd-107">The following example shows an IDL file containing the definition of an interface.</span></span> <span data-ttu-id="a8edd-108">Le corps de la définition d’interface, qui se produit entre les accolades, contient la définition d’une constante (**bufsize**), un type **( \_ \_ type de handle PCONTEXT**) et certaines procédures distantes (**RemoteOpen**, **RemoteRead**, **RemoteClose** et **Shutdown**).</span><span class="sxs-lookup"><span data-stu-id="a8edd-108">The body of the interface definition, which occurs between the curly brackets, contains the definition of a constant (**BUFSIZE**), a type (**PCONTEXT\_HANDLE\_TYPE**), and some remote procedures (**RemoteOpen**, **RemoteRead**, **RemoteClose**, and **Shutdown**).</span></span>

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

<span data-ttu-id="a8edd-109">Pour plus d’informations, consultez [Référence du langage MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="a8edd-109">For more information see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 