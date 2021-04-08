---
title: Désactivation de STRICT
description: Pour désactiver la vérification de type STRICTe, définissez le nom du symbole sur non \_ strict. Dans Visual C/C++, vous pouvez également spécifier cette définition sur la ligne de commande ou dans un Makefile en spécifiant/DNO \_ strict comme option du compilateur.
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bfdfef2aa7988576aa4c1e17f002639de98121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674185"
---
# <a name="disabling-strict"></a><span data-ttu-id="01b05-104">Désactivation de STRICT</span><span class="sxs-lookup"><span data-stu-id="01b05-104">Disabling STRICT</span></span>

<span data-ttu-id="01b05-105">Pour désactiver la vérification de type **stricte** , définissez le nom du symbole sur **non \_ strict**.</span><span class="sxs-lookup"><span data-stu-id="01b05-105">To disable **STRICT** type checking, define the symbol name **NO\_STRICT**.</span></span> <span data-ttu-id="01b05-106">Dans Visual C/C++, vous pouvez également spécifier cette définition sur la ligne de commande ou dans un Makefile en spécifiant **/DNO \_ strict** comme option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="01b05-106">In Visual C/C++, you can also specify this definition on the command line or in a makefile by specifying **/DNO\_STRICT** as a compiler option.</span></span>

<span data-ttu-id="01b05-107">Pour **ne définir aucune \_ restriction** au niveau fichier par fichier, insérez une instruction **\# define** avant d’inclure Windows. h :</span><span class="sxs-lookup"><span data-stu-id="01b05-107">To define **NO\_STRICT** on a file-by-file basis, insert a **\#define** statement before including Windows.h:</span></span>


```C++
#define NO_STRICT
#include <windows.h>
```



<span data-ttu-id="01b05-108">Pour de meilleurs résultats, vous devez également définir le niveau d’avertissement pour les messages d’erreur sur au moins **/W3**.</span><span class="sxs-lookup"><span data-stu-id="01b05-108">For best results, you should also set the warning level for error messages to at least **/W3**.</span></span> <span data-ttu-id="01b05-109">Cela est toujours recommandé avec les applications pour Windows, car une pratique de codage qui génère un avertissement (par exemple, en passant un nombre incorrect de paramètres) provoque généralement une erreur irrécupérable au moment de l’exécution si elle n’est pas corrigée.</span><span class="sxs-lookup"><span data-stu-id="01b05-109">This is always advisable with applications for Windows, because a coding practice that causes a warning (for example, passing the wrong number of parameters) usually causes a fatal error at run time if it is not corrected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01b05-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01b05-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01b05-111">Activation du STRICT</span><span class="sxs-lookup"><span data-stu-id="01b05-111">Enabling STRICT</span></span>](enabling-strict.md)
</dt> <dt>

[<span data-ttu-id="01b05-112">Conformité STRICTe</span><span class="sxs-lookup"><span data-stu-id="01b05-112">STRICT Compliance</span></span>](strict-compliance.md)
</dt> </dl>

 

 




