---
description: La classe de fenêtre IME est une classe globale système prédéfinie qui définit l’apparence et le comportement des fenêtres IME standard.
ms.assetid: 0fa01d84-1304-4235-a148-ea5e8dd5d0b3
title: Classe de fenêtre IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faae7fd0135ec894186b4e10df9bc02da66bb933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865501"
---
# <a name="ime-window-class"></a><span data-ttu-id="f4969-103">Classe de fenêtre IME</span><span class="sxs-lookup"><span data-stu-id="f4969-103">IME Window Class</span></span>

<span data-ttu-id="f4969-104">La classe de fenêtre IME est une classe globale système prédéfinie qui définit l’apparence et le comportement des fenêtres IME standard.</span><span class="sxs-lookup"><span data-stu-id="f4969-104">The IME window class is a predefined system global class that defines the appearance and behavior of the standard IME windows.</span></span> <span data-ttu-id="f4969-105">La classe est semblable aux classes de contrôles communs dans le fait que l’application crée une fenêtre de cette classe à l’aide de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="f4969-105">The class is similar to common control classes in that the application creates a window of this class by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="f4969-106">À l’instar des contrôles statiques, une fenêtre IME ne répond pas aux entrées d’utilisateur par elle-même.</span><span class="sxs-lookup"><span data-stu-id="f4969-106">Like static controls, an IME window does not respond to user input by itself.</span></span> <span data-ttu-id="f4969-107">Au lieu de cela, il avertit l’IME des actions d’entrée d’utilisateur et traite les messages de contrôle qui lui sont envoyés par l’IME ou les applications pour effectuer une réponse à l’action de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4969-107">Instead, it notifies the IME of user input actions and processes control messages sent to it by the IME or applications to carry out a response to the user action.</span></span>

<span data-ttu-id="f4969-108">Les applications prenant en charge l’IME créent parfois des fenêtres IME personnalisées à l’aide de la classe de fenêtre IME.</span><span class="sxs-lookup"><span data-stu-id="f4969-108">IME-aware applications sometimes create customized IME windows using the IME window class.</span></span> <span data-ttu-id="f4969-109">L’utilisation de la personnalisation de fenêtre permet à l’application de tirer parti du traitement par défaut de la fenêtre IME tout en contrôlant le positionnement de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f4969-109">Use of window customization allows the application to take advantage of the default processing of the IME window while having control of window positioning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4969-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f4969-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4969-111">À propos du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="f4969-111">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 
