---
description: Les fonctions suivantes sont utilisées avec les contextes de périphérique.
ms.assetid: 9ff68d16-0f27-4cc8-932a-b2063cfed135
title: Fonctions de contexte de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 625b81b999526d84af4b58f2dddbc280643bcd35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127415960"
---
# <a name="device-context-functions"></a>Fonctions de contexte de périphérique

Les fonctions suivantes sont utilisées avec les contextes de périphérique.



| Fonction                                                   | Description                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc)                               | Annule toute opération en attente sur le contexte de périphérique spécifié.                                                                            |
| [**ChangeDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsa)     | Remplace les paramètres du périphérique d’affichage par défaut par le mode graphique spécifié.                                                        |
| [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) | Remplace les paramètres du périphérique d’affichage spécifié par le mode graphique spécifié.                                                      |
| [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)           | Crée un contexte de périphérique de mémoire compatible avec l’appareil spécifié.                                                                     |
| [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)                               | Crée un contexte de périphérique pour un appareil à l’aide du nom spécifié.                                                                           |
| [**Création**](/windows/desktop/api/Wingdi/nf-wingdi-createica)                               | Crée un contexte d’informations pour le périphérique spécifié.                                                                                  |
| [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc)                               | Supprime le contexte de périphérique spécifié.                                                                                                     |
| [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject)                       | Supprime un stylet logique, un pinceau, une police, une image bitmap, une région ou une palette, libérant ainsi toutes les ressources système associées à l’objet.                  |
| [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)           | Récupère les fonctionnalités d’un pilote de périphérique d’imprimante.                                                                                    |
| [**DrawEscape**](/windows/desktop/api/Wingdi/nf-wingdi-drawescape)                           | Fournit des fonctionnalités de dessin de l’affichage vidéo spécifié qui ne sont pas directement disponibles par le biais de l’interface de périphérique graphique.       |
| [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa)           | Récupère des informations sur les périphériques d’affichage d’un système.                                                                              |
| [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa)         | Récupère des informations sur l’un des modes graphiques pour un périphérique d’affichage.                                                               |
| [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa)     | Récupère des informations sur l’un des modes graphiques pour un périphérique d’affichage.                                                               |
| [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects)                         | Énumère les stylets ou les pinceaux disponibles pour le contexte de périphérique spécifié.                                                                |
| [**EnumObjectsProc**](/windows/win32/api/wingdi/nc-wingdi-gobjenumproc)                 | Fonction de rappel définie par l’application utilisée avec la fonction [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) .                                       |
| [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject)               | Récupère un handle vers un objet du type spécifié qui a été sélectionné dans le contexte de périphérique spécifié.                           |
| [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)                                     | Récupère un handle vers un contexte de périphérique d’affichage pour la zone cliente d’une fenêtre spécifiée ou pour la totalité de l’écran.                        |
| [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)                 | Récupère la couleur de pinceau actuelle pour le contexte de périphérique spécifié.                                                                       |
| [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)                                 | Récupère un handle vers un contexte de périphérique d’affichage pour la zone cliente d’une fenêtre spécifiée ou pour la totalité de l’écran.                        |
| [**GetDCOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getdcorgex)                           | Récupère l’origine de traduction finale pour un contexte de périphérique spécifié.                                                                    |
| [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)                     | Récupère la couleur de stylet actuelle pour le contexte de périphérique spécifié.                                                                         |
| [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps)                     | Récupère des informations spécifiques à l’appareil pour l’appareil spécifié.                                                                           |
| [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout)                             | Récupère la disposition d’un contexte de périphérique.                                                                                                 |
| [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject)                             | Récupère des informations pour l’objet Graphics spécifié.                                                                                  |
| [**GetObjectType**](/windows/desktop/api/Wingdi/nf-wingdi-getobjecttype)                     | Récupère le type de l’objet spécifié.                                                                                               |
| [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject)                   | Récupère un handle vers l’un des stylets boursiers, des pinceaux, des polices ou des palettes.                                                                 |
| [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc)                             | Libère un contexte de périphérique, en le libérant pour une utilisation par d’autres applications.                                                                      |
| [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)                                 | Met à jour le contexte de périphérique de l’imprimante ou du traceur spécifié à l’aide des informations spécifiées.                                                  |
| [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)                             | Restaure l’état spécifié d’un contexte de périphérique.                                                                                         |
| [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc)                                   | Enregistre l’état actuel du contexte de périphérique spécifié en copiant les données décrivant les objets sélectionnés et les modes graphiques dans une pile de contexte. |
| [**SélectionnerObjet**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)                       | Sélectionne un objet dans le contexte de périphérique spécifié.                                                                                      |
| [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | Définit la couleur actuelle du pinceau de contexte de périphérique sur la valeur de couleur spécifiée.                                                                 |
| [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)                     | Définit la couleur actuelle du stylet du contexte de périphérique sur la valeur de couleur spécifiée.                                                                   |
| [**SetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout)                             | Définit la disposition d’un contexte de périphérique.                                                                                                     |
| [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)                       | Retourne un handle vers la fenêtre associée à un contexte de périphérique.                                                                          |



 

 

 
