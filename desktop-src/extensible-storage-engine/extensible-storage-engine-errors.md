---
description: 'En savoir plus sur : Erreurs du moteur de stockage extensible'
title: Erreurs du moteur de stockage extensible
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 55c86d51f44414688897d6450adf214a0478f7d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868966"
---
# <a name="extensible-storage-engine-errors"></a><span data-ttu-id="79bbd-103">Erreurs du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="79bbd-103">Extensible Storage Engine Errors</span></span>


<span data-ttu-id="79bbd-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="79bbd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-errors"></a><span data-ttu-id="79bbd-105">Erreurs du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="79bbd-105">Extensible Storage Engine Errors</span></span>

<span data-ttu-id="79bbd-106">Toutes les erreurs possibles retournées par l’API ESE (Extensible Storage Engine) sont définies par le type de données [JET_ERR](./jet-err.md) .</span><span class="sxs-lookup"><span data-stu-id="79bbd-106">All possible errors returned by the Extensible Storage Engine (ESE) API are defined by the [JET_ERR](./jet-err.md) data type.</span></span> <span data-ttu-id="79bbd-107">Pour obtenir la liste des indicateurs d’erreur définis pour cette API, consultez [codes d’erreur du moteur de stockage extensible](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="79bbd-107">For a list of the error flags that are defined for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).</span></span>

<span data-ttu-id="79bbd-108">Dans la documentation de l’API ESE, seules les erreurs les plus importantes sont documentées.</span><span class="sxs-lookup"><span data-stu-id="79bbd-108">Throughout the ESE API documentation, only the most important errors are documented.</span></span> <span data-ttu-id="79bbd-109">Ces erreurs représentent généralement des erreurs d’utilisation de l’API ou des conditions d’erreur très importantes.</span><span class="sxs-lookup"><span data-stu-id="79bbd-109">These errors typically represent API usage errors or very important error conditions.</span></span> <span data-ttu-id="79bbd-110">N’oubliez pas que ces API ESE peuvent également retourner d’autres erreurs qui ne sont pas documentées pour chaque API.</span><span class="sxs-lookup"><span data-stu-id="79bbd-110">Be aware that any of these ESE APIs can also return other errors that are not documented for each API.</span></span> <span data-ttu-id="79bbd-111">Dans ce cas, l’appelant doit simplement gérer l’erreur, comme pour toute autre erreur retournée par l’API.</span><span class="sxs-lookup"><span data-stu-id="79bbd-111">In these cases, the caller should simply handle the error as they would any other error that is returned by the API.</span></span> <span data-ttu-id="79bbd-112">La valeur d’erreur spécifique peut ensuite être utilisée à des fins de diagnostic telles que le suivi.</span><span class="sxs-lookup"><span data-stu-id="79bbd-112">The specific error value may then be used for diagnostic purposes such as tracing.</span></span>

<span data-ttu-id="79bbd-113">En général, une valeur supérieure à zéro doit être interprétée comme un avertissement, une valeur de zéro doit être interprétée comme une réussite et une valeur inférieure à zéro doit être interprétée comme une erreur.</span><span class="sxs-lookup"><span data-stu-id="79bbd-113">In general, a value that is greater than zero should be interpreted as a warning, a value of zero should be interpreted as success, and a value that is less than zero should be interpreted as an error.</span></span> <span data-ttu-id="79bbd-114">Aucun autre modèle dans ces valeurs (par exemple, les plages de valeurs) ne doit être basé sur une application.</span><span class="sxs-lookup"><span data-stu-id="79bbd-114">No other patterns in these values (for example, ranges of values) should be relied upon by an application.</span></span>

<span data-ttu-id="79bbd-115">Lorsque ESE rencontre certaines des erreurs les plus graves, il crée une entrée dans le journal des événements qui contient des détails sur les erreurs.</span><span class="sxs-lookup"><span data-stu-id="79bbd-115">When ESE encounters some of the more serious errors, it creates an event log entry that contains details about the errors.</span></span> <span data-ttu-id="79bbd-116">Le niveau de journalisation peut être contrôlé par les [paramètres du journal des événements](./event-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="79bbd-116">The level of logging can be controlled by [Event Log Parameters](./event-log-parameters.md).</span></span>

<span data-ttu-id="79bbd-117">Certaines applications requièrent la possibilité de retourner des [JET_ERR](./jet-err.md)s en tant que HRESULT.</span><span class="sxs-lookup"><span data-stu-id="79bbd-117">Some applications require the ability to return [JET_ERR](./jet-err.md)s as HRESULTs.</span></span> <span data-ttu-id="79bbd-118">L’exemple C++ suivant montre comment effectuer cette conversion :</span><span class="sxs-lookup"><span data-stu-id="79bbd-118">The following C++ example shows how to make that conversion:</span></span>

```cpp
    #ifndef FACILITY_JET_ERR
    #define FACILITY_JET_ERR 0xE5E
    #endif
    #ifndef HRESULT_FROM_JET_ERR
    #define HRESULT_FROM_JET_ERR( __err )
    (
      ( __err ) == JET_errSuccess ?
      S_OK :
      (
        ( __err ) == JET_errOutOfMemory ?
        E_OUTOFMEMORY :
        MAKE_HRESULT
        (
          (
            ( __err ) < 0 ?
            SEVERITY_ERROR :
            SEVERITY_SUCCESS
          ),
          FACILITY_JET_ERR,
          (
            ( __err ) < 0 ?
            -( __err ) :
            ( __err )
          )
          & 0xFFFF
        )
      )
    )
    
    #endif
```

<span data-ttu-id="79bbd-119">Pour plus d’informations sur la configuration des paramètres système pour la gestion des erreurs, consultez [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="79bbd-119">For information about configuring system parameters for error handling, see [Error Handling Parameters](./error-handling-parameters.md).</span></span>

### <a name="see-also"></a><span data-ttu-id="79bbd-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79bbd-120">See Also</span></span>

[<span data-ttu-id="79bbd-121">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="79bbd-121">Error Handling Parameters</span></span>](./error-handling-parameters.md)

[<span data-ttu-id="79bbd-122">Codes d’erreur du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="79bbd-122">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)

[<span data-ttu-id="79bbd-123">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="79bbd-123">JET_ERR</span></span>](./jet-err.md)
