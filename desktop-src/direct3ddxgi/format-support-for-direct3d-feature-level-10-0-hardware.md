---
description: Cette section spécifie les formats (valeurs [**DXGI_FORMAT_** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) pris en charge dans le matériel 10,0 de niveau de fonctionnalité Direct3D.
ms.assetid: 3C1CCA7D-9F2F-4B1B-8424-BA9C6DED4974
title: Prise en charge des formats du matériel Direct3D de niveau de fonctionnalité 10.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ac95ab0af4c6a2927f6169fbc4f19b468e0e0a73bb7eb1fb051493b5d7c59b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745739"
---
# <a name="format-support-for-direct3d-feature-level-100-hardware"></a>Prise en charge des formats du matériel Direct3D de niveau de fonctionnalité 10.0

Cette section spécifie les formats (valeurs [**DXGI_FORMAT_** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) pris en charge dans le matériel 10,0 de niveau de fonctionnalité Direct3D.

Le tableau récapitule la prise en charge des fonctionnalités à l’aide de la clé suivante.

| Symbole                            | Description                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| **-**                             | Non autorisé ou non disponible.                                                  |
| ![obligatoire](images/letter-r.jpg)  | Un support matériel est requis.                                                 |
| ![facultatif](images/letter-o.jpg)  | Prise en charge du matériel facultative, le format peut ou non être accéléré par le matériel. |
| ![dépendants](images/letter-d.jpg) | Obligatoire si la fonctionnalité facultative associée est prise en charge.                            |

Cette rubrique contient une section par format. Une *cible* de format (tables contenant une ligne par cible) peut être un type de ressource, une fonction intrinsèque HLSL ou une fonctionnalité particulière qui est dépendante d’un format particulier.

Pour vérifier par programmation la prise en charge du format dans D3D11 et D3D12, consultez vérification de la [prise en charge des fonctionnalités matérielles](checking-hardware-feature-support.md).

> [!NOTE] 
> Les nombres des formats sont principalement, mais pas tous, dans l’ordre numérique croissant, &mdash; certains ne sont pas triés par ordre numérique et sont répertoriés avec d’autres formats pertinents. Notez également que les *types* sans type dans un nom de format peuvent signifier un type *partiellement* typé, et non strictement typés (reportez-vous à la section Remarques sur le [format](#format-notes) à la fin de la rubrique).
 
## <a name="dxgi_format_unknownsuplsup-0"></a>DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 0 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a>\_<sup>PC</sup> DXGI_FORMAT_R32G32B32A32 type (1)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 128 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a>DXGI_FORMAT_R32G32B32A32 \_ float<sup>FCS</sup> (2)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 128 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | ![obligatoire](images/letter-r.jpg) |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![facultatif](images/letter-o.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a>DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FCS</sup> (3)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 128 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | ![obligatoire](images/letter-r.jpg) |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | ![facultatif](images/letter-o.jpg) |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a>DXGI_FORMAT_R32G32B32A32 \_ Saint-<sup>FCS</sup> (4)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 128 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | ![obligatoire](images/letter-r.jpg) |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a>\_<sup>PC</sup> DXGI_FORMAT_R32G32B32 type (5)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 96 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a>DXGI_FORMAT_R32G32B32 \_ float<sup>FCS</sup> (6)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 96 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | ![obligatoire](images/letter-r.jpg) |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![facultatif](images/letter-o.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![facultatif](images/letter-o.jpg) |
| RenderTarget | ![facultatif](images/letter-o.jpg) |
| RenderTarget Blendable | ![dépendants](images/letter-d.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![dépendants](images/letter-d.jpg) |
| 8x-échantillonnage RenderTarget | ![dépendants](images/letter-d.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a>DXGI_FORMAT_R32G32B32 \_ uint<sup>FCS</sup> (7)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 96 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | ![obligatoire](images/letter-r.jpg) |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![facultatif](images/letter-o.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | ![facultatif](images/letter-o.jpg) |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![dépendants](images/letter-d.jpg) |
| 8x-échantillonnage RenderTarget | ![dépendants](images/letter-d.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a>DXGI_FORMAT_R32G32B32 \_ Saint-<sup>FCS</sup> (8)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 96 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | ![obligatoire](images/letter-r.jpg) |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![facultatif](images/letter-o.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![dépendants](images/letter-d.jpg) |
| 8x-échantillonnage RenderTarget | ![dépendants](images/letter-d.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a>\_<sup>PC</sup> DXGI_FORMAT_R16G16B16A16 type (9)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a>DXGI_FORMAT_R16G16B16A16 \_ float<sup>FCS</sup> (10)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | ![obligatoire](images/letter-r.jpg) |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a>DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FCS</sup> (11)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![facultatif](images/letter-o.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a>DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FCS</sup> (12)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | ![facultatif](images/letter-o.jpg) |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a>DXGI_FORMAT_R16G16B16A16 \_ ronfler<sup>FCS</sup> (13)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a>DXGI_FORMAT_R16G16B16A16 \_ Saint-<sup>FCS</sup> (14)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a>\_<sup>PC</sup> DXGI_FORMAT_R32G32 type (15)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a>DXGI_FORMAT_R32G32 \_ float<sup>FCS</sup> (16)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | ![obligatoire](images/letter-r.jpg) |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![facultatif](images/letter-o.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a>DXGI_FORMAT_R32G32 \_ uint<sup>FCS</sup> (17)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | ![obligatoire](images/letter-r.jpg) |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | ![facultatif](images/letter-o.jpg) |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a>DXGI_FORMAT_R32G32 \_ Saint-<sup>FCS</sup> (18)
| Cible | Support technique |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | ![obligatoire](images/letter-r.jpg) |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a>\_<sup>PC</sup> DXGI_FORMAT_R32G8X24 type (19)
| Cible | Support technique |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a>DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FCS</sup> (20)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | ![obligatoire](images/letter-r.jpg) |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a>DXGI_FORMAT_R32 \_ \_ FCS X8X24 float \_ (<sup></sup> 21)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![facultatif](images/letter-o.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a>DXGI_FORMAT_X32 \_ \_ G8X24 \_ uint<sup>FCS</sup> (22)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a>\_<sup>PC</sup> DXGI_FORMAT_R10G10B10A2 type (23)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a>DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FCS</sup> (24)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | ![obligatoire](images/letter-r.jpg) |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a>DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FCS</sup> (25)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | ![facultatif](images/letter-o.jpg) |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a>DXGI_FORMAT_R10G10B10 \_ XR de \_ décalage \_ a2 \_ UNORM<sup>FCS</sup> (89)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![facultatif](images/letter-o.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | ![obligatoire](images/letter-r.jpg) |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a>DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a>\_<sup>PC</sup> DXGI_FORMAT_R8G8B8A8 type (27)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a>DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FCS</sup> (28)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | ![obligatoire](images/letter-r.jpg) |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a>DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRVB<sup>FCS</sup> (29)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | ![obligatoire](images/letter-r.jpg) |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a>DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FCS</sup> (30)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | ![facultatif](images/letter-o.jpg) |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a>DXGI_FORMAT_R8G8B8A8 \_ ronfler<sup>FCS</sup> (31)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a>DXGI_FORMAT_R8G8B8A8 \_ Saint-<sup>FCS</sup> (32)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a>\_<sup>PC</sup> DXGI_FORMAT_R16G16 type (33)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a>DXGI_FORMAT_R16G16 \_ float<sup>FCS</sup> (34)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a>DXGI_FORMAT_R16G16 \_ UNORM<sup>FCS</sup> (35)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![facultatif](images/letter-o.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a>DXGI_FORMAT_R16G16 \_ uint<sup>FCS</sup> (36)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | ![facultatif](images/letter-o.jpg) |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a>DXGI_FORMAT_R16G16 \_ ronfler<sup>FCS</sup> (37)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a>DXGI_FORMAT_R16G16 \_ Saint-<sup>FCS</sup> (38)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a>\_<sup>PC</sup> DXGI_FORMAT_R32 type (39)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a>DXGI_FORMAT_D32 \_ float<sup>FCS</sup> (40)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | ![obligatoire](images/letter-r.jpg) |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Échange atomique UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a>DXGI_FORMAT_R32 \_ float<sup>FCS</sup> (41)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | ![obligatoire](images/letter-r.jpg) |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![facultatif](images/letter-o.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a>DXGI_FORMAT_R32 \_ uint<sup>FCS</sup> (42)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon de sortie de flux | ![obligatoire](images/letter-r.jpg) |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | ![facultatif](images/letter-o.jpg) |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a>DXGI_FORMAT_R32 \_ Saint-<sup>FCS</sup> (43)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | ![obligatoire](images/letter-r.jpg) |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a>\_<sup>PC</sup> DXGI_FORMAT_R24G8 type (44)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a>DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FCS</sup> (45)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | ![obligatoire](images/letter-r.jpg) |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a>DXGI_FORMAT_R24 \_ \_ FCS UNORM x8 non \_ typé (46)<sup></sup>
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![facultatif](images/letter-o.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a>DXGI_FORMAT_X24 \_ \_ G8 \_ UINT<sup>FCS</sup> (47)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a>\_<sup>PC</sup> DXGI_FORMAT_R8G8 type (48)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a>DXGI_FORMAT_R8G8 \_ UNORM<sup>FCS</sup> (49)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a>DXGI_FORMAT_R8G8 \_ uint<sup>FCS</sup> (50)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | ![facultatif](images/letter-o.jpg) |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a>DXGI_FORMAT_R8G8 \_ ronfler<sup>FCS</sup> (51)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a>DXGI_FORMAT_R8G8 \_ Saint-<sup>FCS</sup> (52)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a>\_<sup>PC</sup> DXGI_FORMAT_R16 type (53)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a>DXGI_FORMAT_R16 \_ float<sup>FCS</sup> (54)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a>DXGI_FORMAT_D16 \_ UNORM<sup>FCS</sup> (55)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | ![obligatoire](images/letter-r.jpg) |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a>DXGI_FORMAT_R16 \_ UNORM<sup>FCS</sup> (56)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![facultatif](images/letter-o.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a>DXGI_FORMAT_R16 \_ uint<sup>FCS</sup> (57)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | ![facultatif](images/letter-o.jpg) |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a>DXGI_FORMAT_R16 \_ ronfler<sup>FCS</sup> (58)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a>DXGI_FORMAT_R16 \_ Saint-<sup>FCS</sup> (59)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a>\_<sup>PC</sup> DXGI_FORMAT_R8 type (60)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a>DXGI_FORMAT_R8 \_ UNORM<sup>FCS</sup> (61)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a>DXGI_FORMAT_R8 \_ uint<sup>FCS</sup> (62)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | ![facultatif](images/letter-o.jpg) |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a>DXGI_FORMAT_R8 \_ ronfler<sup>FCS</sup> (63)
| Cible | Support technique |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a>DXGI_FORMAT_R8 \_ Saint-<sup>FCS</sup> (64)
| Cible | Support technique |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a>DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a>DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a>DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a>DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a>DXGI_FORMAT_BC1 \_ <sup>PCC</sup> non typé (70)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 4 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc1_unormsupfccsup-71"></a>DXGI_FORMAT_BC1 \_ UNORM<sup>FCC</sup> (71)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 4 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfccsup-72"></a>DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FCC</sup> (72)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 4 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a>DXGI_FORMAT_BC2 \_ <sup>PCC</sup> non typé (73)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc2_unormsupfccsup-74"></a>DXGI_FORMAT_BC2 \_ UNORM<sup>FCC</sup> (74)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfccsup-75"></a>DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FCC</sup> (75)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a>DXGI_FORMAT_BC3 \_ <sup>PCC</sup> non typé (76)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc3_unormsupfccsup-77"></a>DXGI_FORMAT_BC3 \_ UNORM<sup>FCC</sup> (77)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfccsup-78"></a>DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FCC</sup> (78)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a>DXGI_FORMAT_BC4 \_ <sup>PCC</sup> non typé (79)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 4 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc4_unormsupfccsup-80"></a>DXGI_FORMAT_BC4 \_ UNORM<sup>FCC</sup> (80)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 4 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc4_snormsupfccsup-81"></a>DXGI_FORMAT_BC4 \_ ronfler<sup>FCC</sup> (81)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 4 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a>DXGI_FORMAT_BC5 \_ <sup>PCC</sup> non typé (82)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc5_unormsupfccsup-83"></a>DXGI_FORMAT_BC5 \_ UNORM<sup>FCC</sup> (83)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc5_snormsupfccsup-84"></a>DXGI_FORMAT_BC5 \_ ronfler<sup>FCC</sup> (84)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a>DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![facultatif](images/letter-o.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![facultatif](images/letter-o.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a>DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![facultatif](images/letter-o.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![facultatif](images/letter-o.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![facultatif](images/letter-o.jpg) |
| RenderTarget | ![facultatif](images/letter-o.jpg) |
| RenderTarget Blendable | ![facultatif](images/letter-o.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a>\_<sup>PC</sup> DXGI_FORMAT_B8G8R8A8 type (90)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a>DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FCS</sup> (87)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | ![obligatoire](images/letter-r.jpg) |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a>DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRVB<sup>FCS</sup> (91)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![obligatoire](images/letter-r.jpg) |
| Afficher Scan-Out | ![obligatoire](images/letter-r.jpg) |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a>\_<sup>PC</sup> DXGI_FORMAT_B8G8R8X8 type (92)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a>DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FCS</sup> (88)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a>DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRVB<sup>FCS</sup> (93)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![obligatoire](images/letter-r.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | ![obligatoire](images/letter-r.jpg) |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a>DXGI_FORMAT_AYUV<sup>V</sup> (100)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![facultatif](images/letter-o.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![obligatoire](images/letter-r.jpg) |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_y410supvsup-101"></a>DXGI_FORMAT_Y410<sup>V</sup> (101)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![facultatif](images/letter-o.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_y416supvsup-102"></a>DXGI_FORMAT_Y416<sup>V</sup> (102)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![facultatif](images/letter-o.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_nv12supvsup-103"></a>DXGI_FORMAT_NV12<sup>V</sup> (103)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Entrée du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Sortie du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_p010supvsup-104"></a>DXGI_FORMAT_P010<sup>V</sup> (104)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![facultatif](images/letter-o.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![facultatif](images/letter-o.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_p016supvsup-105"></a>DXGI_FORMAT_P016<sup>V</sup> (105)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![facultatif](images/letter-o.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![facultatif](images/letter-o.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a>DXGI_FORMAT_420 \_ <sup>V</sup> opaque (106)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | \- |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Entrée du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Sortie du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a>DXGI_FORMAT_YUY2<sup>V</sup> (107)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_y210supvsup-108"></a>DXGI_FORMAT_Y210<sup>V</sup> (108)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![facultatif](images/letter-o.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_y216supvsup-109"></a>DXGI_FORMAT_Y216<sup>V</sup> (109)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![facultatif](images/letter-o.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_nv11supvsup-110"></a>DXGI_FORMAT_NV11<sup>V</sup> (110)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![facultatif](images/letter-o.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
| Génération automatique de mipmap | \- |
| RenderTarget | ![obligatoire](images/letter-r.jpg) |
| RenderTarget Blendable | ![obligatoire](images/letter-r.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_ai44supvsup-111"></a>DXGI_FORMAT_AI44<sup>V</sup> (111)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![facultatif](images/letter-o.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_ia44supvsup-112"></a>DXGI_FORMAT_IA44<sup>V</sup> (112)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![facultatif](images/letter-o.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_p8supvsup-113"></a>DXGI_FORMAT_P8<sup>V</sup> (113)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | ![facultatif](images/letter-o.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a>DXGI_FORMAT_A8P8<sup>V</sup> (114)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![facultatif](images/letter-o.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Nuanceur LD | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
| RenderTarget Blendable | \- |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | \- |
| 8x-échantillonnage RenderTarget | \- |
| Autre nombre d’échantillons en RT | \- |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a>DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)
| Cible | Assistance |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | ![facultatif](images/letter-o.jpg) |
| Mémoire tampon du vertex assembleur d’entrée | ![facultatif](images/letter-o.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | ![obligatoire](images/letter-r.jpg) |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Nuanceur LD | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![facultatif](images/letter-o.jpg) |
| RenderTarget | ![facultatif](images/letter-o.jpg) |
| RenderTarget Blendable | ![facultatif](images/letter-o.jpg) |
| Sortie fusion Logic op | \- |
| Cible de la profondeur/du stencil | \- |
| UAV et SRV bruts | \- |
| UAV et SRV structurés | \- |
| UAV typé | \- |
| Magasin typé UAV | \- |
| Charge typée UAV | \- |
| UAV Atomic Add | \- |
| Opérations de bits atomiques UAV | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Exchange Atomic UAV | \- |
| Min ou Max signé UAV | \- |
| UAV Atomic non signé min ou Max | \- |
| UC verrouillable | ![obligatoire](images/letter-r.jpg) |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | ![facultatif](images/letter-o.jpg) |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="format-notes"></a>Mettre en forme les notes

L’objectif du format peut passer d’un niveau de fonctionnalité matériel à l’autre.

<dl> <dt>

<sup>L</sup> : format non typé
</dt> <dt>

<sup>PC</sup> : disposition partiellement typée, castable et simple
</dt> <dt>

 <sup>FCS</sup> : mise en page entièrement typée, castable et simple
</dt> <dt>

<sup>FNS</sup> : mise en page entièrement typée, non stable et simple
</dt> <dt>

<sup>PCC</sup> : disposition partiellement typée, castable et complexe
</dt> <dt>

 <sup>FCC</sup> : mise en page entièrement typée, castable et complexe
</dt> <dt>

<sup>FNC</sup> : mise en page entièrement typée, non stable et complexe
</dt> <dt>

<sup>V</sup> : format vidéo
</dt> </dl>

Les mémoires tampons d’arrière-plan et les analyses avec le format [**dxgi \_ \_ \_ float R16G16B16A16**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) contiennent des données de gamma linéaires.

## <a name="related-topics"></a>Rubriques connexes

[Niveaux de fonctionnalité matérielle D3D12](../direct3d12/hardware-feature-levels.md)

[**ID3D10Device::CheckFormatSupport**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-checkformatsupport)

[Guide de programmation pour DXGI](dx-graphics-dxgi-overviews.md)
