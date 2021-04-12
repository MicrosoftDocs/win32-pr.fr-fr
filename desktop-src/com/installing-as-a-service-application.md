---
title: Installation d’une application en tant que service
description: Installation d’une application en tant que service
ms.assetid: 0dd4b348-3d12-49ba-8098-4adb9df01a0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed5c474d73c74b3be40bae773c3d51eadf6c69a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031904"
---
# <a name="installing-as-a-service-application"></a><span data-ttu-id="4e795-103">Installation d’une application en tant que service</span><span class="sxs-lookup"><span data-stu-id="4e795-103">Installing as a Service Application</span></span>

<span data-ttu-id="4e795-104">En plus de s’exécuter en tant qu’exécutable de serveur local (EXE), un objet COM peut également s’empaqueter lui-même pour s’exécuter en tant qu’application de service lorsqu’il est activé par un client local ou distant.</span><span class="sxs-lookup"><span data-stu-id="4e795-104">In addition to running as a local server executable (EXE), a COM object may also package itself to run as a service application when activated by a local or remote client.</span></span> <span data-ttu-id="4e795-105">Les services prennent en charge de nombreuses fonctionnalités d’administration intégrées, telles que le démarrage, l’arrêt, l’interruption et le redémarrage locaux et interface, ainsi que la possibilité d’établir le serveur à exécuter sous un [compte d’utilisateur](/windows/desktop/Services/service-user-accounts) et une [station Windows](/windows/desktop/winstation/window-stations)spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4e795-105">Services support numerous useful and user interfaceâ€“integrated administrative features, including local and remote starting, stopping, pausing, and restarting, as well as the ability to establish the server to run under a specific [user account](/windows/desktop/Services/service-user-accounts) and [window station](/windows/desktop/winstation/window-stations).</span></span>

<span data-ttu-id="4e795-106">Un objet écrit en tant que service est installé pour une utilisation par COM en établissant une valeur [LocalService](localservice.md) sous sa clé [AppID](appid-key.md) et en effectuant une installation de service standard.</span><span class="sxs-lookup"><span data-stu-id="4e795-106">An object written as a service is installed for use by COM by establishing a [LocalService](localservice.md) value under its [AppID](appid-key.md) key and performing a standard service installation.</span></span>

<span data-ttu-id="4e795-107">Les classes peuvent également être configurées pour s’exécuter sous un compte d’utilisateur spécifique lorsqu’elles sont activées par un client distant sans être écrites en tant qu’application de service.</span><span class="sxs-lookup"><span data-stu-id="4e795-107">Classes may also be configured to run under a specific user account when activated by a remote client without being written as a service application.</span></span> <span data-ttu-id="4e795-108">Pour ce faire, la classe installe un nom d’utilisateur et un mot de passe à utiliser lorsque le SCM lance son processus serveur local.</span><span class="sxs-lookup"><span data-stu-id="4e795-108">To do this, the class installs a user name and a password to be used when the SCM launches its local server process.</span></span>

<span data-ttu-id="4e795-109">Quand une classe est configurée de cette manière, les appels à [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) avec ce CLSID échouent, sauf si le processus a été lancé par com pour le compte d’une demande d’activation réelle.</span><span class="sxs-lookup"><span data-stu-id="4e795-109">When a class is configured in this fashion, calls to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) with this CLSID will fail unless the process was launched by COM on behalf of an actual activation request.</span></span> <span data-ttu-id="4e795-110">En d’autres termes, les classes configurées pour s’exécuter en tant qu’utilisateur particulier peuvent ne pas être enregistrées sous une autre identité.</span><span class="sxs-lookup"><span data-stu-id="4e795-110">In other words, classes configured to run as a particular user may not be registered under any other identity.</span></span>

<span data-ttu-id="4e795-111">Le nom d’utilisateur est extrait de la valeur nommée [runas](runas.md) sous la clé AppID de la classe.</span><span class="sxs-lookup"><span data-stu-id="4e795-111">The user name is taken from the [RunAs](runas.md) named-value under the class's APPID key.</span></span> <span data-ttu-id="4e795-112">Si le nom d’utilisateur est « utilisateur interactif », le code de la classe est exécuté dans le contexte de sécurité de l’utilisateur actuellement connecté et est connecté à la station Windows Interactive.</span><span class="sxs-lookup"><span data-stu-id="4e795-112">If the user name is "Interactive User", the class code is run in the security context of the currently logged on user and is connected to the interactive window station.</span></span>

<span data-ttu-id="4e795-113">Dans le cas contraire, le mot de passe est récupéré à partir d’une partie cachée du Registre, accessible uniquement aux administrateurs de l’ordinateur et au système.</span><span class="sxs-lookup"><span data-stu-id="4e795-113">Otherwise, the password is retrieved from a hidden portion of the registry available only to administrators of the machine and to the system.</span></span> <span data-ttu-id="4e795-114">Le nom d’utilisateur et le mot de passe sont ensuite utilisés pour créer une session de connexion dans laquelle le code de la classe est exécuté.</span><span class="sxs-lookup"><span data-stu-id="4e795-114">The user name and password are then used to create a logon session in which the class code is run.</span></span> <span data-ttu-id="4e795-115">Lorsqu’il est lancé de cette manière, le code de la classe s’exécute avec son propre bureau et sa propre station de travail et ne partage pas les handles de fenêtre, le presse-papiers ou d’autres éléments de l’interface utilisateur avec l’utilisateur interactif ou d’autres classes s’exécutant dans d’autres comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4e795-115">When launched in this way, the class code runs with its own desktop and window-station and does not share window handles, the clipboard, or other user interface elements with the interactive user or other classes running in other user accounts.</span></span>

<span data-ttu-id="4e795-116">Un serveur inscrit avec **LocalService** ou **runas** peut inscrire un objet dans la table d’objets en cours d’exécution pour permettre à n’importe quel client de s’y connecter.</span><span class="sxs-lookup"><span data-stu-id="4e795-116">A server registered either with **LocalService** or **RunAs** can register an object in the running object table to allow any client to connect to it.</span></span> <span data-ttu-id="4e795-117">Pour ce faire, l’appel du serveur à [**IRunningObjectTable :: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) doit définir l' \_ indicateur ROTFLAGS ALLOWANYCLIENT.</span><span class="sxs-lookup"><span data-stu-id="4e795-117">To do so, the server's call to [**IRunningObjectTable::Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) must set the ROTFLAGS\_ALLOWANYCLIENT flag.</span></span> <span data-ttu-id="4e795-118">Un paramètre de serveur doit avoir son nom d’exécutable dans la section AppID du Registre qui fait référence à l’AppID pour l’exécutable.</span><span class="sxs-lookup"><span data-stu-id="4e795-118">A server setting this bit must have its executable name in the AppID section of the registry that refers to the AppID for the executable.</span></span> <span data-ttu-id="4e795-119">Un serveur « Activate As Activator » (non inscrit comme **LocalService** ou **runas**) ne peut pas inscrire un objet avec cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="4e795-119">An "activate as activator" server (not registered as either **LocalService** or **RunAs**) may not register an object with this flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e795-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4e795-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e795-121">Inscription d’une classe lors de l’installation</span><span class="sxs-lookup"><span data-stu-id="4e795-121">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="4e795-122">Inscription d’un serveur exécutable en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="4e795-122">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
</dt> <dt>

[<span data-ttu-id="4e795-123">Inscription d’objets dans le ROT</span><span class="sxs-lookup"><span data-stu-id="4e795-123">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> <dt>

[<span data-ttu-id="4e795-124">Inscription automatique</span><span class="sxs-lookup"><span data-stu-id="4e795-124">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 