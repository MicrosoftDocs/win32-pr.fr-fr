---
title: LocalService
description: Installe un objet en tant qu’application de service.
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- Valeur de Registre LocalService COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f630c7c0a6f5e3bbf4b9c26ad82e5a104be238
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842794"
---
# <a name="localservice"></a><span data-ttu-id="f3df2-104">LocalService</span><span class="sxs-lookup"><span data-stu-id="f3df2-104">LocalService</span></span>

<span data-ttu-id="f3df2-105">Installe un objet en tant qu’application de service.</span><span class="sxs-lookup"><span data-stu-id="f3df2-105">Installs an object as a service application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="f3df2-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="f3df2-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LocalService = name
```

## <a name="remarks"></a><span data-ttu-id="f3df2-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f3df2-107">Remarks</span></span>

<span data-ttu-id="f3df2-108">En plus de s’exécuter en tant qu’exécutable de serveur local (EXE), un objet COM peut également choisir de s’empaqueter pour s’exécuter en tant qu’application de service lorsqu’il est activé par un client local ou distant.</span><span class="sxs-lookup"><span data-stu-id="f3df2-108">In addition to running as a local server executable (EXE), a COM object may also choose to package itself to run as a service application when activated by a local or remote client.</span></span> <span data-ttu-id="f3df2-109">Les services prennent en charge de nombreuses fonctionnalités d’administration utiles et intégrées à l’interface utilisateur, notamment le démarrage, l’arrêt, l’interruption et le redémarrage locaux et distants, ainsi que la possibilité d’établir le serveur pour qu’il s’exécute sous un compte d’utilisateur et une station Windows spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f3df2-109">Services support numerous useful and UI-integrated administrative features, including local and remote starting, stopping, pausing, and restarting, as well as the ability to establish the server to run under a specific user account and window station.</span></span>

<span data-ttu-id="f3df2-110">Un objet écrit en tant que service est installé pour une utilisation par COM en établissant une valeur **LocalService** et en effectuant une installation de service standard.</span><span class="sxs-lookup"><span data-stu-id="f3df2-110">An object written as a service is installed for use by COM by establishing a **LocalService** value and performing a standard service installation.</span></span> <span data-ttu-id="f3df2-111">La valeur **LocalService** doit être définie sur le nom du service, tel que configuré dans **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ services**, en tant que valeur par défaut de **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="f3df2-111">The **LocalService** value must be set to the service name, as configured in **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services**, as the default **REG\_SZ** value.</span></span>

<span data-ttu-id="f3df2-112">Lorsque **LocalService** est défini, toute chaîne assignée à [**ServiceParameters**](serviceparameters.md) est passée comme argument de ligne de commande au service lors de son lancement.</span><span class="sxs-lookup"><span data-stu-id="f3df2-112">When **LocalService** is set, any string assigned to [**ServiceParameters**](serviceparameters.md) is passed as a command-line argument to the service as it is being launched.</span></span>

<span data-ttu-id="f3df2-113">La configuration du service est préférable dans de nombreux cas où les fonctionnalités des API de gestion des services locale et distante et de l’interface utilisateur peuvent être utiles pour les services fournis par l’objet.</span><span class="sxs-lookup"><span data-stu-id="f3df2-113">The service configuration is preferred in many situations where the capabilities of the local and remote service management APIs and user interface might be useful for the services that the object provides.</span></span> <span data-ttu-id="f3df2-114">Par exemple, l’utilisation de l’infrastructure administrative existante de l’architecture de service doit être un choix évident si l’objet est de longue durée ou prend en charge des concepts tels que le démarrage, l’arrêt, la réinitialisation ou la suspension.</span><span class="sxs-lookup"><span data-stu-id="f3df2-114">For example, leveraging the existing administrative framework of the service architecture should be an obvious choice if the object is long-lived or readily supports concepts such as starting, stopping, resetting, or pausing.</span></span>

<span data-ttu-id="f3df2-115">Les services peuvent être configurés de manière dynamique et peuvent être configurés pour s’exécuter automatiquement lors du démarrage de l’ordinateur, ou pour être lancés à la demande d’une application cliente.</span><span class="sxs-lookup"><span data-stu-id="f3df2-115">Services can be dynamically configured and can be configured to run automatically when the machine boots, or to be launched when requested by a client application.</span></span>

<span data-ttu-id="f3df2-116">Si vous implémentez des classes en tant que services, vous devez être conscient des points suivants :</span><span class="sxs-lookup"><span data-stu-id="f3df2-116">If you are implementing classes as services, you should be aware of the following points:</span></span>

-   <span data-ttu-id="f3df2-117">Cette valeur est utilisée par préférence à la clé [**LocalServer32**](localserver32.md) pour l’activation locale et à distance requestsâ. Si **LocalService** existe et qu’il fait référence à un service valide, la clé **LocalServer32** est ignorée.</span><span class="sxs-lookup"><span data-stu-id="f3df2-117">This value is used in preference to the [**LocalServer32**](localserver32.md) key for local and remote activation requestsâ€”if **LocalService** exists and refers to a valid service, the **LocalServer32** key is ignored.</span></span>
-   <span data-ttu-id="f3df2-118">Actuellement, une seule instance d’une application de service peut s’exécuter à un moment donné sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3df2-118">Currently, only a single instance of a service application may be running at a given time on a computer.</span></span> <span data-ttu-id="f3df2-119">Les services COM doivent donc inscrire leurs objets de classe au lancement à l’aide \_ de REGCLS MULTIPLEUSE pour prendre en charge plusieurs clients.</span><span class="sxs-lookup"><span data-stu-id="f3df2-119">COM services must therefore register their class objects on launch using REGCLS\_MULTIPLEUSE to support multiple clients.</span></span>
-   <span data-ttu-id="f3df2-120">Pour lancer et initialiser correctement, les services COM configurés pour s’exécuter automatiquement lorsqu’un ordinateur démarre doivent inclure RPCSS dans leur liste de services dépendants.</span><span class="sxs-lookup"><span data-stu-id="f3df2-120">To launch and initialize properly, COM services configured to run automatically when a machine boots must include RPCSS in their list of dependent services.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3df2-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3df2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3df2-122">Inscription des serveurs COM</span><span class="sxs-lookup"><span data-stu-id="f3df2-122">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="f3df2-123">**ServiceParameters**</span><span class="sxs-lookup"><span data-stu-id="f3df2-123">**ServiceParameters**</span></span>](serviceparameters.md)
</dt> <dt>

[<span data-ttu-id="f3df2-124">Services</span><span class="sxs-lookup"><span data-stu-id="f3df2-124">Services</span></span>](/windows/desktop/Services/services)
</dt> </dl>

 

 