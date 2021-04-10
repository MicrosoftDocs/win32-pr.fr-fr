---
title: Plateforme de capteur
description: Windows 7 a changé la façon dont les développeurs utilisent les capteurs.
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fe94fd48ffa16080054a22b4d377ab4757d61d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031477"
---
# <a name="sensor-platform"></a><span data-ttu-id="d67c5-103">Plateforme de capteur</span><span class="sxs-lookup"><span data-stu-id="d67c5-103">Sensor Platform</span></span>

<span data-ttu-id="d67c5-104">Windows 7 a changé la façon dont les développeurs utilisent les capteurs.</span><span class="sxs-lookup"><span data-stu-id="d67c5-104">Windows 7 has changed how developers use sensors.</span></span> <span data-ttu-id="d67c5-105">Il inclut la prise en charge native des capteurs, développée par une nouvelle plateforme de développement pour l’utilisation de capteurs, y compris les capteurs d’emplacement, tels que les périphériques GPS (Global Positioning Systems).</span><span class="sxs-lookup"><span data-stu-id="d67c5-105">It includes native support for sensors, expanded by a new development platform for working with sensors, including location sensors, such as Global Positioning Systems (GPS) devices.</span></span>

<span data-ttu-id="d67c5-106">Reposant sur la plateforme de capteur, les API d' *emplacement Windows* sont une nouvelle fonctionnalité de Windows 7 qui permet aux développeurs d’applications d’accéder aux informations relatives à l’emplacement physique de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d67c5-106">Built on the Sensor Platform, the *Windows Location* APIs are a new Windows 7 feature that enables application developers to access the user's physical location information.</span></span> <span data-ttu-id="d67c5-107">Les API d' *emplacement Windows* peuvent faire abstraction du matériel, prendre en charge simultanément plusieurs applications et basculer en toute transparence entre les différentes technologies, ce qui allège le développeur d’applications de la charge de gestion de ces contraintes.</span><span class="sxs-lookup"><span data-stu-id="d67c5-107">The *Windows Location* APIs can abstract hardware, simultaneously support multiple applications, and seamlessly switch between different technologies, relieving the application developer of the burden of managing these constraints.</span></span> <span data-ttu-id="d67c5-108">Les API de *localisation* peuvent être utilisées par les programmeurs par le biais du langage de programmation C++ (par les programmeurs habitués au modèle com), ou en utilisant des objets COM dans des langages de script, tels que Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="d67c5-108">The *Location* APIs can be used by programmers through the C++ programming language (by programmers familiar with Component Object Model (COM)), or by using COM objects in scripting languages, such as Microsoft JScript.</span></span> <span data-ttu-id="d67c5-109">La prise en charge des scripts permet d’accéder facilement aux données de localisation des projets tels que les gadgets.</span><span class="sxs-lookup"><span data-stu-id="d67c5-109">Scripting support gives easy access to location data for projects such as gadgets.</span></span>

<span data-ttu-id="d67c5-110">Windows 7 fournit une plate-forme solide et facile à utiliser pour l’utilisation de périphériques de capteur, tels qu’un capteur de lumière ambiante ou une jauge de température, afin de créer une prise en compte de l’environnement dans les applications Windows.</span><span class="sxs-lookup"><span data-stu-id="d67c5-110">Windows 7 provides a solid, easy-to-use platform for using sensor devices, such as an ambient light sensor or a temperature gauge, to create environmental awareness in Windows applications.</span></span> <span data-ttu-id="d67c5-111">Les PC peuvent utiliser des capteurs intégrés à l’ordinateur, connectés par le biais de connexions câblées ou sans fil, ou connectés via un réseau ou *Internet*.</span><span class="sxs-lookup"><span data-stu-id="d67c5-111">PCs can use sensors that are built into the computer, connected through wired or wireless connections, or connected through a network or the *Internet*.</span></span>

<span data-ttu-id="d67c5-112">Les API de *capteur* et de *localisation* offrent un moyen standard de découvrir les capteurs et d’accéder par programmation aux données fournies par les capteurs.</span><span class="sxs-lookup"><span data-stu-id="d67c5-112">The *Sensor* and *Location* APIs provide a standard way to discover sensors, and to programmatically access data that sensors provide.</span></span>

<span data-ttu-id="d67c5-113">Le panneau de configuration du *capteur* permet aux utilisateurs d’activer ou de désactiver les capteurs, de contrôler l’accès aux capteurs susceptibles d’exposer des données sensibles, d’afficher les propriétés de capteur et de modifier la description des capteurs.</span><span class="sxs-lookup"><span data-stu-id="d67c5-113">The *Sensor* control panel lets users enable or disable sensors, control access to sensors that might expose sensitive data, view sensor properties, and change the descriptions of sensors.</span></span>

<span data-ttu-id="d67c5-114">L' [extension de classe de capteur](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) est une partie fondamentale du modèle de développement de pilote pour la plateforme de capteur.</span><span class="sxs-lookup"><span data-stu-id="d67c5-114">The [Sensor Class Extension](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) is a core part of the driver development model for the Sensor Platform.</span></span> <span data-ttu-id="d67c5-115">Il fournit les mécanismes suivants, qui sont utilisés lors de l’écriture d’un pilote de capteur de l' [infrastructure de pilote en mode utilisateur (UMDF)](https://developer.microsoft.com/windows/hardware) :</span><span class="sxs-lookup"><span data-stu-id="d67c5-115">It provides the following mechanisms, which are used when writing a [User-Mode Driver Framework (UMDF)](https://developer.microsoft.com/windows/hardware) sensor driver:</span></span>

-   <span data-ttu-id="d67c5-116">Intégration à la plateforme de capteur</span><span class="sxs-lookup"><span data-stu-id="d67c5-116">Integration with the Sensor Platform</span></span>
-   <span data-ttu-id="d67c5-117">Mise en œuvre de la sécurité</span><span class="sxs-lookup"><span data-stu-id="d67c5-117">Security enforcement</span></span>

## <a name="related-topics"></a><span data-ttu-id="d67c5-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d67c5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d67c5-119">API de capteur</span><span class="sxs-lookup"><span data-stu-id="d67c5-119">Sensor API</span></span>](../sensorsapi/portal.md)
</dt> <dt>