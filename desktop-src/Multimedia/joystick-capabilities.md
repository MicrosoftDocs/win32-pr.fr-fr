---
title: Fonctionnalités de la manette de jeu
description: Fonctionnalités de la manette de jeu
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- entrée multimédia, joysticks
- joysticks, déplacement sur deux axes
- joysticks, déplacement sur trois axes
- manettes, boutons
- joysticks, plages de mouvement
- joysticks, fréquences d’interrogation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b317d5a0c8deb48b49224fd051ecb7ce5a0bbced
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726717"
---
# <a name="joystick-capabilities"></a><span data-ttu-id="aa838-109">Fonctionnalités de la manette de jeu</span><span class="sxs-lookup"><span data-stu-id="aa838-109">Joystick Capabilities</span></span>

<span data-ttu-id="aa838-110">Les manettes peuvent prendre en charge le déplacement sur deux ou trois axes et jusqu’à quatre boutons.</span><span class="sxs-lookup"><span data-stu-id="aa838-110">Joysticks can support two- or three-axis movement and up to four buttons.</span></span> <span data-ttu-id="aa838-111">Les joysticks prennent également en charge différentes plages de *fréquences d’interrogation* et *de mouvement* .</span><span class="sxs-lookup"><span data-stu-id="aa838-111">Joysticks also support different *ranges of motion* and *polling frequencies*.</span></span> <span data-ttu-id="aa838-112">La plage de mouvement est la distance à laquelle un handle de manette de jeu peut passer de sa position de repos à la position la plus éloignée de sa position de repos.</span><span class="sxs-lookup"><span data-stu-id="aa838-112">The range of motion is the distance a joystick handle can move from its resting position to the position farthest from its resting position.</span></span> <span data-ttu-id="aa838-113">La fréquence d’interrogation est l’intervalle de temps entre les requêtes de manette de jeu.</span><span class="sxs-lookup"><span data-stu-id="aa838-113">The polling frequency is the time interval between joystick queries.</span></span>

<span data-ttu-id="aa838-114">Les pilotes de manette de jeu peuvent prendre en charge une ou deux manettes.</span><span class="sxs-lookup"><span data-stu-id="aa838-114">Joystick drivers can support either one or two joysticks.</span></span> <span data-ttu-id="aa838-115">Vous pouvez déterminer le nombre de joysticks pris en charge par un pilote de manette de jeu à l’aide de la fonction [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) .</span><span class="sxs-lookup"><span data-stu-id="aa838-115">You can determine the number of joysticks supported by a joystick driver by using the [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) function.</span></span> <span data-ttu-id="aa838-116">Cette fonction retourne un entier non signé qui contient le nombre de joysticks pris en charge ou zéro s’il n’y a pas de prise en charge de la manette de jeu.</span><span class="sxs-lookup"><span data-stu-id="aa838-116">This function returns an unsigned integer that contains the number of supported joysticks or zero if there is no joystick support.</span></span> <span data-ttu-id="aa838-117">La valeur de retour n’indique pas le nombre de joysticks attachés au système.</span><span class="sxs-lookup"><span data-stu-id="aa838-117">The return value does not indicate the number of joysticks attached to the system.</span></span>

<span data-ttu-id="aa838-118">Vous pouvez déterminer si une manette de jeu est attachée au système à l’aide de la fonction [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) .</span><span class="sxs-lookup"><span data-stu-id="aa838-118">You can determine if a joystick is attached to the system by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) function.</span></span> <span data-ttu-id="aa838-119">Cette fonction retourne \_ l’erreur JOYERR si l’appareil spécifié est attaché.</span><span class="sxs-lookup"><span data-stu-id="aa838-119">This function returns JOYERR\_NOERROR if the specified device is attached.</span></span> <span data-ttu-id="aa838-120">Sinon, elle retourne JOYERR \_ débranché.</span><span class="sxs-lookup"><span data-stu-id="aa838-120">Otherwise , it returns JOYERR\_UNPLUGGED.</span></span>

<span data-ttu-id="aa838-121">Chaque manette de jeu offre plusieurs fonctionnalités qui sont disponibles pour votre application.</span><span class="sxs-lookup"><span data-stu-id="aa838-121">Each joystick has several capabilities that are available to your application.</span></span> <span data-ttu-id="aa838-122">Vous pouvez récupérer les fonctionnalités d’une manette de jeu à l’aide de la fonction [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="aa838-122">You can retrieve the capabilities of a joystick by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function.</span></span> <span data-ttu-id="aa838-123">Cette fonction remplit une structure [**JoyCaps**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) avec des fonctionnalités de manette de jeu telles que les valeurs minimale et maximale de son système de coordonnées, le nombre de boutons sur la manette de jeu et les fréquences d’interrogation minimale et maximale.</span><span class="sxs-lookup"><span data-stu-id="aa838-123">This function fills a [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) structure with joystick capabilities such as the minimum and maximum values for its coordinate system, the number of buttons on the joystick, and the minimum and maximum polling frequencies.</span></span>

 

 