---
description: Cette section spécifie les formats (valeurs [**DXGI_FORMAT_** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) qui sont pris en charge dans la fonctionnalité Direct3D 10Level9 9,3 Hardware.
ms.assetid: B2A843D5-6A6B-4180-8B94-D032B1322798
title: Prise en charge des formats du matériel Direct3D de niveau de fonctionnalité 9.3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79185ddb360fe9359371671e3722372c3a1615f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232668"
---
# <a name="format-support-for-direct3d-feature-10level9-93-hardware"></a>Prise en charge des formats du matériel Direct3D de niveau de fonctionnalité 9.3

Cette section spécifie les formats (valeurs [**DXGI_FORMAT_** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) qui sont pris en charge dans la fonctionnalité Direct3D 10Level9 9,3 Hardware.

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
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 0 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a>\_<sup>PC</sup> DXGI_FORMAT_R32G32B32A32 type (1)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 128 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a>DXGI_FORMAT_R32G32B32A32 \_ float<sup>FNS</sup> (2)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 128 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
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
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a>DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FNS</sup> (3)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 128 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a>DXGI_FORMAT_R32G32B32A32 \_ Saint<sup>FNS</sup> (4)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 128 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a>\_<sup>PC</sup> DXGI_FORMAT_R32G32B32 type (5)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 96 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a>DXGI_FORMAT_R32G32B32 \_ float<sup>FNS</sup> (6)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 96 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
| Génération automatique de mipmap | \- |
| RenderTarget | \- |
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
| UC verrouillable | \- |
| RenderTarget multiéchantillon 4x | ![dépendants](images/letter-d.jpg) |
| 8x-échantillonnage RenderTarget | ![dépendants](images/letter-d.jpg) |
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

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a>DXGI_FORMAT_R32G32B32 \_ uint<sup>FNS</sup> (7)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 96 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| RenderTarget multiéchantillon 4x | ![dépendants](images/letter-d.jpg) |
| 8x-échantillonnage RenderTarget | ![dépendants](images/letter-d.jpg) |
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

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a>DXGI_FORMAT_R32G32B32 \_ Saint<sup>FNS</sup> (8)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 96 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| RenderTarget multiéchantillon 4x | ![dépendants](images/letter-d.jpg) |
| 8x-échantillonnage RenderTarget | ![dépendants](images/letter-d.jpg) |
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

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a>\_<sup>PC</sup> DXGI_FORMAT_R16G16B16A16 type (9)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a>DXGI_FORMAT_R16G16B16A16 \_ float<sup>FNS</sup> (10)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a>DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FNS</sup> (11)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a>DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FNS</sup> (12)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a>DXGI_FORMAT_R16G16B16A16 \_ ronfler<sup>FNS</sup> (13)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a>DXGI_FORMAT_R16G16B16A16 \_ Saint<sup>FNS</sup> (14)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a>\_<sup>PC</sup> DXGI_FORMAT_R32G32 type (15)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a>DXGI_FORMAT_R32G32 \_ float<sup>FNS</sup> (16)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | \- |
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
| Résolution d’échantillonnages | ![obligatoire](images/letter-r.jpg) |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a>DXGI_FORMAT_R32G32 \_ uint<sup>FNS</sup> (17)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a>DXGI_FORMAT_R32G32 \_ Saint<sup>FNS</sup> (18)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a>\_<sup>PC</sup> DXGI_FORMAT_R32G8X24 type (19)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a>DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FNS</sup> (20)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a>DXGI_FORMAT_R32 \_ float \_ X8X24 \_ de type<sup>FNS</sup> (21)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a>DXGI_FORMAT_X32 \_ \_ G8X24 \_ uint<sup>FNS</sup> (22)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 64 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a>\_<sup>PC</sup> DXGI_FORMAT_R10G10B10A2 type (23)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a>DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FNS</sup> (24)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a>DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FNS</sup> (25)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a>DXGI_FORMAT_R10G10B10 \_ XR \_ \_ de décalage a2 \_ UNORM<sup>FNS</sup> (89)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a>DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a>\_<sup>PC</sup> DXGI_FORMAT_R8G8B8A8 type (27)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a>DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FNS</sup> (28)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | ![obligatoire](images/letter-r.jpg) |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a>DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRVB<sup>FNS</sup> (29)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | ![obligatoire](images/letter-r.jpg) |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a>DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FNS</sup> (30)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a>DXGI_FORMAT_R8G8B8A8 \_ ronfler<sup>FNS</sup> (31)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a>DXGI_FORMAT_R8G8B8A8 \_ Saint<sup>FNS</sup> (32)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a>\_<sup>PC</sup> DXGI_FORMAT_R16G16 type (33)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a>DXGI_FORMAT_R16G16 \_ float<sup>FNS</sup> (34)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
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
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a>DXGI_FORMAT_R16G16 \_ UNORM<sup>FNS</sup> (35)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a>DXGI_FORMAT_R16G16 \_ uint<sup>FNS</sup> (36)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a>DXGI_FORMAT_R16G16 \_ ronfler<sup>FNS</sup> (37)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a>DXGI_FORMAT_R16G16 \_ Saint<sup>FNS</sup> (38)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a>\_<sup>PC</sup> DXGI_FORMAT_R32 type (39)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a>DXGI_FORMAT_D32 \_ float<sup>FNS</sup> (40)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a>DXGI_FORMAT_R32 \_ float<sup>FNS</sup> (41)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | \- |
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
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a>DXGI_FORMAT_R32 \_ uint<sup>FNS</sup> (42)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a>DXGI_FORMAT_R32 \_ Saint<sup>FNS</sup> (43)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a>\_<sup>PC</sup> DXGI_FORMAT_R24G8 type (44)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a>DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FNS</sup> (45)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| UC verrouillable | \- |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a>DXGI_FORMAT_R24 \_ UNORM \_ x8 \_ de type<sup>FNS</sup> (46)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a>DXGI_FORMAT_X24 \_ \_ G8 \_ UINT<sup>FNS</sup> (47)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a>\_<sup>PC</sup> DXGI_FORMAT_R8G8 type (48)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a>DXGI_FORMAT_R8G8 \_ UNORM<sup>FNS</sup> (49)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a>DXGI_FORMAT_R8G8 \_ uint<sup>FNS</sup> (50)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a>DXGI_FORMAT_R8G8 \_ ronfler<sup>FNS</sup> (51)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a>DXGI_FORMAT_R8G8 \_ Saint<sup>FNS</sup> (52)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a>\_<sup>PC</sup> DXGI_FORMAT_R16 type (53)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a>DXGI_FORMAT_R16 \_ float<sup>FNS</sup> (54)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a>DXGI_FORMAT_D16 \_ UNORM<sup>FNS</sup> (55)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| UC verrouillable | \- |
| RenderTarget multiéchantillon 4x | ![facultatif](images/letter-o.jpg) |
| 8x-échantillonnage RenderTarget | ![facultatif](images/letter-o.jpg) |
| Autre nombre d’échantillons en RT | ![facultatif](images/letter-o.jpg) |
| Résolution d’échantillonnages | \- |
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a>DXGI_FORMAT_R16 \_ UNORM<sup>FNS</sup> (56)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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

## <a name="dxgi_format_r16_uintsupfnssup-57"></a>DXGI_FORMAT_R16 \_ uint<sup>FNS</sup> (57)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | ![obligatoire](images/letter-r.jpg) |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a>DXGI_FORMAT_R16 \_ ronfler<sup>FNS</sup> (58)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a>DXGI_FORMAT_R16 \_ Saint<sup>FNS</sup> (59)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a>\_<sup>PC</sup> DXGI_FORMAT_R8 type (60)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a>DXGI_FORMAT_R8 \_ UNORM<sup>FNS</sup> (61)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a>DXGI_FORMAT_R8 \_ uint<sup>FNS</sup> (62)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a>DXGI_FORMAT_R8 \_ ronfler<sup>FNS</sup> (63)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a>DXGI_FORMAT_R8 \_ Saint<sup>FNS</sup> (64)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a>DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a>DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a>DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a>DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 16 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a>DXGI_FORMAT_BC1 \_ <sup>PCC</sup> non typé (70)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 4 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a>DXGI_FORMAT_BC1 \_ UNORM<sup>FNC</sup> (71)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 4 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a>DXGI_FORMAT_BC1 \_ UNORM \_ sRVB<sup>FNC</sup> (72)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 4 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a>DXGI_FORMAT_BC2 \_ <sup>PCC</sup> non typé (73)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a>DXGI_FORMAT_BC2 \_ UNORM<sup>FNC</sup> (74)
| Cible | Support |
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
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a>DXGI_FORMAT_BC2 \_ UNORM \_ sRVB<sup>FNC</sup> (75)
| Cible | Support |
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
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a>DXGI_FORMAT_BC3 \_ <sup>PCC</sup> non typé (76)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a>DXGI_FORMAT_BC3 \_ UNORM<sup>FNC</sup> (77)
| Cible | Support |
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
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a>DXGI_FORMAT_BC3 \_ UNORM \_ sRVB<sup>FNC</sup> (78)
| Cible | Support |
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
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a>DXGI_FORMAT_BC4 \_ <sup>PCC</sup> non typé (79)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 4 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a>DXGI_FORMAT_BC4 \_ UNORM<sup>FNC</sup> (80)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 4 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a>DXGI_FORMAT_BC4 \_ ronfler<sup>FNC</sup> (81)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 4 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a>DXGI_FORMAT_BC5 \_ <sup>PCC</sup> non typé (82)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a>DXGI_FORMAT_BC5 \_ UNORM<sup>FNC</sup> (83)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a>DXGI_FORMAT_BC5 \_ ronfler<sup>FNC</sup> (84)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 8 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a>DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)
| Cible | Support |
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
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a>DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)
| Cible | Support |
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
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a>\_<sup>PC</sup> DXGI_FORMAT_B8G8R8A8 type (90)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a>DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FNS</sup> (87)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | ![obligatoire](images/letter-r.jpg) |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a>DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRVB<sup>FNS</sup> (91)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | ![obligatoire](images/letter-r.jpg) |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![obligatoire](images/letter-r.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a>\_<sup>PC</sup> DXGI_FORMAT_B8G8R8X8 type (92)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | \- |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a>DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FNS</sup> (88)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a>DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRVB<sup>FNS</sup> (93)
| Cible | Support |
| - | - |
| Bits par élément (BPE) | 32 |
| Prise en charge du format | ![obligatoire](images/letter-r.jpg) |
| Buffer | \- |
| Mémoire tampon du vertex assembleur d’entrée | \- |
| Tampon d’index assembleur d’entrée | \- |
| Mémoire tampon de sortie de flux | \- |
| Texture1D | \- |
| Texture2D | ![obligatoire](images/letter-r.jpg) |
| Texture3D | ![obligatoire](images/letter-r.jpg) |
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
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
| Charge d’échantillonnage | \- |
| Afficher Scan-Out | \- |
| Cast dans la disposition binaire | \- |
| Prise en charge du décodeur vidéo | \- |
| Entrée du processeur vidéo | \- |
| Sortie du processeur vidéo | \- |
| Ressource partagée | ![obligatoire](images/letter-r.jpg) |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a>DXGI_FORMAT_AYUV<sup>V</sup> (100)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_y410supvsup-101"></a>DXGI_FORMAT_Y410<sup>V</sup> (101)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_y416supvsup-102"></a>DXGI_FORMAT_Y416<sup>V</sup> (102)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_nv12supvsup-103"></a>DXGI_FORMAT_NV12<sup>V</sup> (103)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_p010supvsup-104"></a>DXGI_FORMAT_P010<sup>V</sup> (104)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_p016supvsup-105"></a>DXGI_FORMAT_P016<sup>V</sup> (105)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a>DXGI_FORMAT_420 \_ <sup>V</sup> opaque (106)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a>DXGI_FORMAT_YUY2<sup>V</sup> (107)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_y210supvsup-108"></a>DXGI_FORMAT_Y210<sup>V</sup> (108)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_y216supvsup-109"></a>DXGI_FORMAT_Y216<sup>V</sup> (109)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_nv11supvsup-110"></a>DXGI_FORMAT_NV11<sup>V</sup> (110)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Prise en charge du décodeur vidéo | ![facultatif](images/letter-o.jpg) |
| Entrée du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Sortie du processeur vidéo | ![facultatif](images/letter-o.jpg) |
| Ressource partagée | \- |
| Ressource en mosaïque | \- |

## <a name="dxgi_format_ai44supvsup-111"></a>DXGI_FORMAT_AI44<sup>V</sup> (111)
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Cible | Support |
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
| Exemple de nuanceur (échantillon de point uniquement) | \- |
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
| Cible | Support |
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
| TextureCube | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (échantillon de point uniquement) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur (n’importe quel filtre) | ![obligatoire](images/letter-r.jpg) |
| Exemple de nuanceur \_ c (filtre de comparaison) | \- |
| Exemple de nuanceur (filtre mono 1 bit) | \- |
| Nuanceur gather4 | \- |
| Nuanceur gather4 \_ c | \- |
| MIP | ![obligatoire](images/letter-r.jpg) |
| Génération automatique de mipmap | ![facultatif](images/letter-o.jpg) |
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

## <a name="related-topics"></a>Rubriques connexes

[Niveaux de fonctionnalité matérielle D3D12](../direct3d12/hardware-feature-levels.md)

[Implémentation de mémoires tampons secondaires pour le niveau de fonctionnalité Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10))

[Mappage des formats hérités](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[Guide de programmation pour DXGI](dx-graphics-dxgi-overviews.md)
